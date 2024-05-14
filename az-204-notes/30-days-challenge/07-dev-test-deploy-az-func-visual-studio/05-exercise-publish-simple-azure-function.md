# Exercise: Publish a Simple Azure Function

## Overview

In this exercise, you'll learn how to deploy an Azure Function using Visual Studio. You'll create an Azure Function App in the Azure portal and then publish the WatchInfo function from Visual Studio to this app. Finally, you'll verify that the function is correctly deployed by testing it.

### Prerequisites

- Access to the Azure portal with appropriate permissions.
- Visual Studio 2022 installed on your machine.
- Basic understanding of Azure Functions and Visual Studio.

## Step 1: Create an Azure Function App using the Azure Portal

1. **Sign in to the Azure Portal**: Use your account credentials to sign in to the Azure portal.

2. **Create a Resource**: Navigate to the "Create a resource" option and select "Function App" under the "Compute" category.

3. **Configure Function App**: Fill in the required details, such as function app name, subscription, resource group, runtime stack, version, region, and plan type. Ensure that you select the appropriate options according to your requirements.

4. **Review and Create**: Review your configurations and create the function app. Wait for the deployment to complete.

## Step 2: Deploy the WatchInfo Function to the Azure Function App

1. **Open Visual Studio**: Return to Visual Studio and open the solution containing your Azure Function project.

2. **Publish the Project**: Right-click on the project in the Solution Explorer and select "Publish". Choose the Azure target, select "Azure Function App (Windows)", and specify your subscription and function app.

3. **Initiate Publish**: Click on "Publish" to start the deployment process. Monitor the progress in the Output window of Visual Studio.

## Step 3: Verify Deployment

1. **Check Azure Portal**: Return to the Azure portal and navigate to your Function App. Verify that both the Function1 and WatchInfo functions are listed under "Functions".

2. **Verify Status**: Check the overview section of the Function App to ensure that it's running successfully.

3. **Test the Function**: Click on the URL of the Function App to open it in a browser. Append "/api/watchinfo" to the URL to invoke the WatchInfo function without a query string. Verify that the function returns the expected response.

4. **Test with Query String**: Append "?model=abc" to the URL and refresh the browser window. Confirm that the function returns the details of the watch model specified in the query string.

## Conclusion

In this exercise, you successfully deployed an Azure Function to the cloud using Visual Studio. You learned how to create an Azure Function App in the Azure portal, publish the function from Visual Studio, and verify its deployment and functionality.
