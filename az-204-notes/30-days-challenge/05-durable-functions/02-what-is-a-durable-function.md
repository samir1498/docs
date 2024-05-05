# What is Durable Functions?

Durable Functions allows you to implement complex stateful functions in a serverless environment.

## Example Scenario

Your company currently follows a manual approval process for project-design proposals. The process has multiple steps, and each step in the process can vary in duration. Implementing an automated process in-house is complex and costly. Coordinating each step takes effort. In addition, you must be able to incorporate custom logic into the workflow.

## Durable Functions

Durable Functions is an extension of Azure Functions. Whereas Azure Functions operates in a stateless environment, Durable Functions can retain state between function calls. This approach allows you to simplify complex stateful executions in a serverless environment.

Durable Functions scales as needed and provides a cost-effective means of implementing complex workflows in the cloud. Some benefits of using Durable Functions include:

- They enable you to write event-driven code.
- You can chain functions together.
- You can orchestrate and coordinate functions and specify the order in which functions should execute.
- The state is managed for you.

### Orchestration Functions

Durable Functions allows you to define stateful workflows using an orchestration function. An orchestration function provides these extra benefits:

- You can define the workflows in code.
- Functions can be called both synchronously and asynchronously.
- Azure checkpoints the progress of a function automatically when the function awaits.

## Function Types

You can use three durable function types: Client, Orchestrator, and Activity.

- **Client functions:** Entry points for creating an instance of a Durable Functions orchestration.
- **Orchestrator functions:** Describe how actions are executed and the order in which they're run.
- **Activity functions:** Basic units of work in a Durable Functions orchestration.

## Application Patterns

You can use Durable Functions to implement many common workflow patterns, including:

- Function chaining
- Fan out/fan in
- Async HTTP APIs
- Monitor
- Human interaction

## Comparison with Logic Apps

Durable Functions and Logic Apps are both Azure services that enable serverless workload. Azure Durable Functions is intended as a powerful serverless compute option to run custom logic, while Azure Logic Apps are better suited for integrating Azure services and components. Each has its own development approach and set of capabilities.

### Key Differences

| Task        | Azure Durable Functions                           | Azure Logic Apps                                      |
|-------------|---------------------------------------------------|-------------------------------------------------------|
| Development | Code-first (imperative)                          | Design-first (declarative)                            |
| Connectivity| About a dozen built-in binding types              | Large collection of connectors                         |
| Actions     | Each activity is an Azure Function                | Large collection of ready-made actions                |
| Monitoring  | Azure Application Insights                        | Azure portal, Azure Monitor logs                       |
| Management  | REST API, PowerShell, Visual Studio               | Azure portal, REST API, PowerShell, Visual Studio      |

## Check your knowledge

1. **What is Durable Functions?**

   Durable Functions is an extension of Azure Functions that allows you to simplify complex stateful executions in a serverless environment.

2. **Which of the following best describes the role of the Orchestrator function in a workflow?**

   It's used for describing how actions are executed and the order in which actions are executed.

3. **Which of the following best explains why the Human Interaction application pattern benefits from Durable Functions?**

   A manual process within an automated process because people aren't as highly available and as responsive as computers.
