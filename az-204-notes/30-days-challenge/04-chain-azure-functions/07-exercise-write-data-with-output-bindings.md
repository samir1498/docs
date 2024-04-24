# Exercise - Write Data with Output Bindings

## Overview

In this exercise, we'll enhance our Azure Function to not only read bookmarks from an Azure Cosmos DB but also write new bookmarks to it. Additionally, we'll set up an output binding to push messages to an Azure Queue Storage for further processing.

## Steps

1. **Create an HTTP-Triggered Function**: Set up an HTTP-triggered function in your function app.

2. **Configure Azure Cosmos DB Input Binding**: Add an input binding to retrieve data from the Azure Cosmos DB collection.

3. **Configure Azure Cosmos DB Output Binding**: Set up an output binding to write new entries to the Azure Cosmos DB collection.

4. **Set Up Azure Queue Storage Output Binding**: Configure an output binding to send messages to an Azure Queue Storage queue.

5. **Update Function Implementation**: Replace the function code with the provided snippet to handle adding bookmarks and pushing messages to the queue.

6. **Test the Function**: Send HTTP requests to add bookmarks and verify that messages are successfully written to the queue for processing.

## Summary

This exercise demonstrates the use of output bindings to facilitate writing data to Azure Cosmos DB and Azure Queue Storage. By leveraging output bindings, you can streamline the integration of your function with various data sources and services, minimizing the need for complex code and manual management of connections.
