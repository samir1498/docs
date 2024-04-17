
# Exercise - Add logic to the function app

## Introduction

In this exercise, we will build a serverless temperature service using Azure Functions. The service will receive temperature data via HTTP requests and categorize them based on predefined criteria.

## Function Requirements

- Temperatures from 0 up to 25 degrees should be flagged as OK.
- Temperatures above 25 up to 50 degrees should be flagged as CAUTION.
- Temperatures above 50 degrees should be flagged as DANGER.

## Adding a Function to the Function App

1. Open your Azure Function App in the Azure portal.
2. Navigate to the Functions tab and select "Create" to add a new function.
3. Choose the HTTP trigger template.
4. Name your function and select "Create."

## Implementing the Function Logic

1. Navigate to the "Code + Test" section of your function in the Azure portal.
2. Replace the default code in the `index.js` file with the provided JavaScript code:

```javascript
module.exports = function (context, req) {
    context.log('Drive Gear Temperature Service triggered');
    if (req.body && req.body.readings) {
        req.body.readings.forEach(function(reading) {

            if(reading.temperature<=25) {
                reading.status = 'OK';
            } else if (reading.temperature<=50) {
                reading.status = 'CAUTION';
            } else {
                reading.status = 'DANGER'
            }
            context.log('Reading is ' + reading.status);
        });

        context.res = {
            // status: 200, /* Defaults to 200 */
            body: {
                "readings": req.body.readings
            }
        };
    }
    else {
        context.res = {
            status: 400,
            body: "Please send an array of readings in the request body"
        };
    }
    context.done();
};
```

## Testing the Function

1. Expand the Logs section at the bottom of the function pane.
2. Obtain the function URL by selecting "Get function URL" from the command bar.
3. Use cURL to send HTTP requests to the function URL.
4. Test with various temperature values and observe the response.

### Testing Data

Sample request body for testing:

```json
{
    "readings": [
        {
            "driveGearId": 1,
            "timestamp": 1534263995,
            "temperature": 23
        },
        {
            "driveGearId": 3,
            "timestamp": 1534264048,
            "temperature": 45
        },
        {
            "driveGearId": 18,
            "timestamp": 1534264050,
            "temperature": 55
        }
    ]
}
```


## Securing HTTP Triggers

- HTTP triggers can be secured using API keys.
- By default, the authorization level is set to Function, requiring a function-specific API key.
- You can also set it to Admin for a global "master" key or Anonymous for no key requirement.

## Monitoring and Logging

- Monitor function invocations using the Monitor section in the Azure portal.
- View invocation traces to analyze the execution of your function.
