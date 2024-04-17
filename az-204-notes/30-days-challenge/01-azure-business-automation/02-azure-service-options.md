# Identify the Technology Options for Business Process Automation in Azure

## Common Business Issues

In business, maintaining high-quality products and services often requires well-defined and integrated business processes. However, issues arise when merging with another business or integrating with a partner organization, especially when dealing with disparate software systems.

### Workflow Technologies in Azure

Azure offers four main technologies for building and implementing workflows:

1. **Logic Apps**
2. **Microsoft Power Automate**
3. **WebJobs**
4. **Azure Functions**

### Key Features

- **Inputs:** Accept data or files.
- **Actions:** Perform operations, potentially modifying data.
- **Conditions:** Make decisions based on inputs.
- **Outputs:** Produce data or files.

Workflows can start based on schedules or external events.

## Design-First Technologies

### Logic Apps

- Platform for automating and integrating components of distributed applications.
- Offers a visual designer for workflow creation.
- Supports over 200 connectors for integrating with external services.
- Allows editing workflows in JSON notation for advanced customization.

### Microsoft Power Automate

- Enables workflow creation without development or IT expertise.
- Offers four flow types: automated, button, scheduled, and business process.
- Provides a user-friendly design surface for workflow creation.
- Built on Logic Apps, supporting the same range of connectors and actions.

## Code-First Technologies

### WebJobs

- Part of Azure App Service for running programs or scripts automatically.
- Types include continuous and triggered.
- Supports C# if you're using the WebJobs SDK.
- Offers WebJobs SDK for easier interaction with Azure App Service.

### Azure Functions

- Serverless solution for running small pieces of code in the cloud.
- Supports multiple languages including C#, Java, and JavaScript.
- Offers templates for different trigger types such as HTTP, timer, blob storage, and Cosmos DB.
- Automatically scales based on demand and follows a pay-per-use pricing model.

## Technology Comparison

### Design-First Technologies Comparison

|                     | Microsoft Power Automate | Logic Apps                |
|---------------------|--------------------------|---------------------------|
| Intended Users      | Office workers, business analysts | Developers, IT pros        |
| Intended Scenarios  | Self-service workflow creation  | Advanced integration projects |
| Design Tools        | GUI only (browser and mobile app) | Browser and Visual Studio designer, code editing possible |
| Application Lifecycle Management | Testing and production environments included | Source code management possible with Azure DevOps |
|                     |                          |                            |

### Code-First Technologies Comparison

|                     | Azure WebJobs            | Azure Functions           |
|---------------------|--------------------------|---------------------------|
| Supported Languages | C# (with WebJobs SDK)    | C#, Java, JavaScript, PowerShell, and more |
| Automatic Scaling   | No                       | Yes                        |
| Development Testing in Browser | No               | Yes                        |
| Pay-per-use Pricing | No                       | Yes                        |
| Integration with Logic Apps | No                  | Yes                        |
| Package Managers    | NuGet (with WebJobs SDK) | NuGet and NPM              |
| Part of App Service Application | Yes             | Yes (hosted under App Service plan) |
| Provides Close Control of JobHost | Yes            | No                         |

Now that you have an understanding of the available technologies, you can begin to narrow down your choices based on your specific requirements and preferences.

---
