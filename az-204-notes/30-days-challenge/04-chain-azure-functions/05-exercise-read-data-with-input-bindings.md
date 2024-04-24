# Exercise - Read data with input bindings

## Introduction

In this exercise, you'll learn how to read data from an Azure Cosmos DB database using Azure Functions and input bindings. Input bindings allow you to configure connections to external data sources without writing code explicitly to handle connections.

## Create an Azure Cosmos DB account

### Create a database account

To begin, you need to create a database account in Azure Cosmos DB.

1. Navigate to the Azure portal and select "Create a resource" from the resource menu.
2. Search for and select "Azure Cosmos DB" under Databases.
3. Choose "Azure Cosmos DB for NoSQL" and click "Create" to proceed.
4. Fill in the required details on the Basics tab, such as Subscription, Resource Group, Account Name, and Location.
5. Review your input and create the database account.
6. Wait for the deployment to complete.

### Add a container

After creating the database account, you'll need to add a container to store your data.

1. Access the Data Explorer tool within your Azure Cosmos DB account.
2. Select "New Container" and provide necessary details like Database id, Database Max RU/s, Container id, and Partition key.
3. Allow some time for the container to be created.

### Add test data

Now, populate the container with some test data.

1. Navigate to the Items tab within the Bookmarks container.
2. Add items by selecting "New Item" and entering JSON code for each item, including "id" and "url" properties.
3. Save each item to populate the container with data.

## Create your function

### Verify the function

Ensure your function app is set up and functioning properly.

1. Access your function app in the Azure portal.
2. If necessary, create a new function using the HTTP trigger template.
3. Verify the function by testing it with a personalized response.

### Add an Azure Cosmos DB input binding

To read data from the Azure Cosmos DB, you'll need to define an input binding.

1. In the Azure portal, navigate to the Integration section of your function.
2. Add an input binding by selecting "Add input" and choosing "Azure Cosmos DB" from the dropdown.
3. Configure the binding details, including Document parameter name, Database name, Collection Name, Document ID, and Partition key.
4. Save the input binding configuration.

### Update the function implementation

Modify your function's code to utilize the input binding.

1. Update the function's code to retrieve data from the input binding.
2. Handle cases where data is found or not found in the database.
3. Save the changes to the function implementation.

### Modify your function's JSON implementation code

Update the function's JSON configuration to accept parameters from the query string.

1. Modify the values for "id" and "partitionKey" in the function.json file to accept parameters.
2. Save the changes to the JSON configuration.

## Try it out

Test your function to ensure it correctly reads data from the Azure Cosmos DB.

1. Obtain the function URL and append the query string parameter for the bookmark ID.
2. Run the request and observe the response.
3. Test with different bookmark IDs to verify the function's behavior.

## Conclusion

In this exercise, you learned how to set up an Azure Cosmos DB account, add data, create an Azure Function with input bindings, and retrieve data from the database. Input bindings simplify the process of connecting to external data sources, reducing the amount of code you need to write.
