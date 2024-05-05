# Control Long-Running Tasks Using Timers

When dealing with long-running workflows, it's essential to handle scenarios where tasks might not complete within an acceptable timeframe. Durable Functions offer a solution to this challenge through durable timers, allowing you to implement timeouts and escalation paths.

## Timers in Durable Functions

Durable Functions provide timers for orchestrator functions, enabling you to introduce delays or set timeouts for asynchronous actions. It's recommended to use durable timers instead of traditional `setTimeout()` and `setInterval()` functions.

### Using Timers for Delay

You can utilize durable timers to introduce delays in your workflow. The following example demonstrates how to send a reminder every day for 10 days:

```javascript
const df = require("durable-functions");
const moment = require("moment");

module.exports = df.orchestrator(function*(context) {
    for (let i = 0; i < 10; i++) {
        const deadline = moment.utc(context.df.currentUtcDateTime).add(i, 'd');
        yield context.df.createTimer(deadline.toDate());
        yield context.df.callActivity("SendReminder");
    }
});
```

Always use `currentUtcDateTime` to obtain the current date and time instead of `Date.now` or `Date.UTC`.

#### Using Timers for Timeout

You can also use durable timers to implement timeouts. The following example demonstrates how to wait until either an activity function completes or a deadline timer expires:

```javascript
const df = require("durable-functions");
const moment = require("moment");

module.exports = df.orchestrator(function*(context) {
    const deadline = moment.utc(context.df.currentUtcDateTime).add(30, "s");

    const activityTask = context.df.callActivity("GetQuote");
    const timeoutTask = context.df.createTimer(deadline.toDate());

    const winner = yield context.df.Task.any([activityTask, timeoutTask]);
    if (winner === activityTask) {
        // Success case
        timeoutTask.cancel();
        return true;
    } else {
        // Timeout case
        return false;
    }
});
```

### Exercise: Adding Escalation Path

In the next exercise, you'll use the information provided here to add an escalation path to the orchestrator function in our sample scenario. This escalation path will handle scenarios where a project design proposal isn't approved in a timely manner.

By leveraging durable timers, you can ensure that your workflows are robust and responsive to various scenarios, including timeouts and delays.
