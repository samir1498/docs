# Exercise Overview: Creating and Testing an Azure Function Locally

In this exercise, you'll utilize Visual Studio to develop and test an Azure Function App locally. The objective is to create a function that returns detailed information about a watch based on its model number.

## Prerequisites

Make sure you have Visual Studio 2022 installed, along with the following workloads:

- ASP.NET and web development
- Azure development

## Steps

1. **Create an Azure Function App:**
   - Launch Visual Studio and select "Create a new project".
   - Choose the Azure Functions template.
   - Configure the project with the desired settings, including the project name, location, and solution name.
   - Select .NET 6.0 as the Dotnet version.
   - Choose HTTP trigger as the function trigger.
   - Use Azurite for runtime storage account.
   - Set the authorization level to Anonymous.
   - Create the project.

2. **Create the WatchInfo Azure Function:**
   - In Solution Explorer, right-click on the project and select "Add" > "New Azure Function".
   - Name the function `WatchInfo.cs` and choose HTTP trigger with Anonymous access.
   - Visual Studio creates the function with a `Run` method annotated with `[FunctionName("WatchInfo")]`.

3. **Implement the Functionality:**
   - Modify the `Run` method in `WatchInfo.cs` to retrieve the model id from the query string.
   - If a model id is provided, return detailed information about the watch based on dummy data.
   - If no model id is provided, return an error message.

4. **Test the Azure Function Locally:**
   - Start debugging the project in Visual Studio.
   - Once the Azure Functions runtime is ready, navigate to the URL displayed in the runtime window.
   - Test the function with and without providing a model id in the query string.
   - Verify that the function returns the expected results and handles errors appropriately.
   - Debug the function locally to ensure correct behavior under different scenarios.
   - Stop debugging once testing is complete.

This exercise demonstrates how Visual Studio simplifies the development and testing of Azure Functions locally, allowing you to iterate quickly and ensure the functionality meets your requirements.
