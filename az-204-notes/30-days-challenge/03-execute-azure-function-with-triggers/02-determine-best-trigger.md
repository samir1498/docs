# Determine the Best Trigger for Your Azure Function

A function in Azure Functions needs something to tell it when to run. For example, we could create a function to send out text messages before appointments. If we don't tell the function when to run, it won't run.

This unit describes triggers at a high level, explores the most common types of triggers, and uses bindings to connect a trigger to a function.

## What is a trigger?

A trigger is an object that defines a specific function. For example, if you want a function to execute every 10 minutes, you could use a timer trigger.

Every function must have exactly one trigger associated with it. If you want to execute a piece of logic that runs under multiple conditions, you need to create multiple functions that share the same core function code.

In this module, we're going to focus on three trigger types: timer, HTTP, and blob.

## Types of Triggers

Azure Functions supports a wide range of trigger types:

- **Timer:** Execute a function at a set interval
- **HTTP:** Execute a function when an HTTP request is received
- **Blob:** Execute a function when a file is uploaded or updated
- **Queue:** Execute a function when a message is added to an Azure Storage queue
- **Azure Cosmos DB:** Execute a function when a document changes in a collection
- **Azure SQL:** Execute a function when a row changes in a table
- **Event Hub:** Execute a function when an event hub receives a new event
- **Event Grid:** Execute a function based on Event Grid subscriptions

## What is a Binding?

A binding is a connection to data within your function. Bindings are optional and can be input bindings, output bindings, or both. An input binding lets your function read data from another service, while an output binding lets your function write data to another service.

Unlike a trigger, a function can have multiple input bindings and output bindings. If you choose not to use bindings at all, you can still access services using client SDKs.

## What is a Function App?

Azure Functions lets you group one or more functions into a single function app. All functions in a function app share the same resources, app settings, and deployments.

In the next exercise, we'll run a function on a schedule using a Timer trigger.
