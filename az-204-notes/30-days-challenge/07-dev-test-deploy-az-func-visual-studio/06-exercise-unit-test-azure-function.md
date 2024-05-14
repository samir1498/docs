# Exercise: Unit Test an Azure Function

Unit testing is crucial for ensuring the reliability and correctness of your Azure Functions. In this exercise, you'll learn how to create unit tests for Azure Functions using the xUnit test framework in Visual Studio.

## Prerequisites

- Visual Studio installed on your machine.
- Basic understanding of Azure Functions and unit testing concepts.

## Step 1: Create a Unit Test Project

1. **Create a Project**: Right-click on the solution in Solution Explorer, select "Add", then "New Project".

2. **Choose Template**: Select the xUnit Test Project template.

3. **Configure Project**: Name the project "WatchFunctionsTests" and ensure it's located in the same folder as your Azure Function project.

4. **Install Packages**: Install the "Microsoft.AspNetCore.Mvc" package via NuGet Package Manager.

5. **Add Project Reference**: Reference the Azure Function project by right-clicking on "Dependencies" under the test project and selecting "Add Project Reference".

## Step 2: Add Unit Tests for the WatchInfo Function

1. **Open Test File**: Double-click on the "WatchFunctionUnitTests.cs" file in Solution Explorer.

2. **Add Using Directives**: Include necessary using directives for HTTP context and logging.

3. **Create Test Methods**: Add test methods to ensure the WatchInfo function behaves correctly under different scenarios:
   - **TestWatchFunctionSuccess**: Verifies successful response with a model parameter in the query string.
   - **TestWatchFunctionFailureNoQueryString**: Verifies failure response when no query string is provided.
   - **TestWatchFunctionFailureNoModel**: Verifies failure response when the query string doesn't contain the model parameter.

4. **Run Tests**: Execute the tests by selecting "Run All Tests" from the Test menu. Ensure all tests pass.

## Step 3: Run Tests with Modified Code (Optional)

1. **Modify Code**: Introduce intentional error in the WatchInfo function code.

2. **Re-run Tests**: Execute the tests again to observe failure due to the introduced error.

## Conclusion

In this exercise, you learned how to create and execute unit tests for Azure Functions using Visual Studio and the xUnit framework. By ensuring adequate test coverage, you can improve the reliability and quality of your Azure Functions.
