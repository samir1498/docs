# Summary

This module focused on integrating data and services into your functions. It began with an overview of the various binding types available when adding them to a function. Subsequently, it delved into reading data from an Azure Cosmos DB using input bindings, highlighting the ease of managing connection strings and accessing data in code. Finally, the module concentrated on writing data to different sources with the assistance of output bindings.

The journey through this module is summarized in the following table, outlining the different bindings utilized in each learning unit:

| Learning Unit                          | Triggers | Input Bindings | Output Bindings |
|----------------------------------------|----------|----------------|-----------------|
| Explore input and output binding types | HTTP     | HTTP           | HTTP            |
| Read data with input bindings          | HTTP     | HTTP           |                 |
|                                        |          | Azure Cosmos DB|                 |
| Write data with output bindings        | HTTP     | HTTP           |                 |
|                                        |          |                | Azure Cosmos DB|
|                                        |          |                | Azure Queue Storage |

This module provided foundational knowledge and practical exercises to add and test bindings in functions. To further enhance your skills and build on this foundation, consider the following ideas:

1. Create additional functions to read from Blob storage and other input binding types.
2. Implement functions to write to various destinations using different supported output binding types.
3. Extend the functionality by adding another function to process messages from the queue and perform specific actions based on the message content.
4. Explore Azure Logic Apps for serverless integrations with visual workflows and minimal custom code.

Remember to clean up resources after completing your work to avoid unnecessary costs. The sandbox environment automatically handles resource cleanup, but in your own subscription, it's essential to delete resources no longer needed.

For further exploration, refer to the provided additional resources, including Azure Functions documentation, Azure Serverless Computing Cookbook, and specific documentation for Azure Cosmos DB and Azure Queue Storage.

## Check your knowledge

1. **Advantages of Bindings**: Bindings provide a declarative way to connect to data, simplifying the connection process and eliminating the need for coding specific connection logic.

2. **Function Configuration File**: The file containing function configuration data is named `function.json`, which includes JSON configuration data such as binding declarations.

3. **Triggers in Functions**: A function must have exactly one trigger.
