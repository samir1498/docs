# Summary: Creating Serverless Logic with Azure Functions

In this module, you learned how to leverage Azure Functions to host business logic services in the cloud.

- Azure Functions provide a convenient way to add hosted services to your solution that can scale and adapt to the needs of your business. By focusing on writing code in the language of your choice, Azure takes care of managing the underlying infrastructure.

- Azure Functions can seamlessly integrate with other Azure services like Event Grid, GitHub, Twilio, Microsoft Graph, and Logic Apps, enabling you to create complex and robust serverless workflows quickly and easily.

## Important Note

When working with Azure resources in this module, it's essential to clean up these resources to avoid ongoing charges. You can delete resources individually or delete the entire resource group to remove all associated resources.

---

## Check Your Knowledge

1. **Which of the following best defines serverless logic?**

   - Code you write that doesn't run on servers.

   - Code you write that runs on servers you manage.

   - Code you write that runs on servers a cloud provider manages.

   **Answer:** Serverless doesn't mean there are no servers - it just means the developer doesn't have to worry about servers. Instead, a cloud provider such as Azure, manages servers.

2. **The container that groups functions into a logical unit for easier management, deployment, and sharing of resources is called?**

   - Resource group

   - Function app

   - Function collection

   **Answer:** A function app is a way to organize one or more individual functions and collectively manage them with Azure App Service. All the functions in a function app share the same pricing plan, continuous deployment, and runtime version.

3. **We secured our function against unknown HTTP callers by requiring a function-specific API key be passed with each call. Which of the following fields is the header name in the HTTP requests that needs to contain this key?**

   - x-functions-key

   - x-requested-with

   - x-csrf-token

   **Answer:** The API key can be included as a query string parameter named code or as an HTTP header named x-functions-key.
