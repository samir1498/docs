# Run an Azure Function on a Schedule

Imagine you run a blog and want to send a weekly newsletter to your subscribers. You can use a timer trigger to execute a function on a schedule, without having to write a bunch of complex code.

**What is a Timer Trigger?**

A timer trigger is a trigger that executes a function at a consistent interval. It requires two pieces of information:

1. A Timestamp parameter name, simply an identifier to access the trigger in code.
2. A Schedule, represented by a CRON expression, setting the interval for the timer.

**What is a CRON Expression?**

A CRON expression is a string representing a set of times. In Azure Functions, the order of the six fields is: {second} {minute} {hour} {day} {month} {day of the week}.

For instance, a CRON expression to execute every five minutes looks like: `0 */5 * * * *`

To build a CRON expression, you need to understand some special characters:

- `*`: Selects every value in a field.
- `,`: Separates items in a list.
- `-`: Specifies a range.
- `/`: Specifies an increment.

## How to Create a Timer Trigger

You can create a timer trigger in the Azure portal. Select timer trigger from the list of trigger templates, provide the logic to execute, and input the Timestamp parameter name and the CRON expression.

This module focuses on creating triggers in the portal, but you can also create triggers programmatically using Core Tools, Visual Studio, or Visual Studio Code.

A timer trigger invokes the function code on a consistent schedule, defined by a CRON expression.

**Next unit:** Exercise - Create a timer trigger
