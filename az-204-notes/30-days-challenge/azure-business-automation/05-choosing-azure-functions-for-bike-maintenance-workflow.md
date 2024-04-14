# Choosing Azure Functions for Bike Maintenance Workflow

## Scenario Overview

In this scenario, you aim to streamline the bike maintenance and repair process to ensure high-quality rental service. The goal is to implement a system that tracks bike maintenance status, part orders, and availability for rental.

## Business Process Workflow

- Customer returns a bike, triggering the maintenance process.
- Technician marks the bike as unavailable and performs checks.
- If new parts are required:
  - Technician orders new parts.
  - Parts arrive, and the technician fits them.
- Final checks are completed, and the bike is marked as available for rent.

## Technology Options

You have the following Azure technologies to implement the workflow and integrate with existing systems:

1. **Microsoft Power Automate**
2. **Azure Logic Apps**
3. **Azure Functions**
4. **Azure App Service WebJobs**

## Decision Criteria

### Design-first or code-first?

- **Requirement:** Need to access inventory system and place orders with third-party parts company.
- **Choice:** Code-first approach to provide flexibility and integration capabilities.

### Azure Functions or Azure App Service WebJobs?

- **Cost:** Azure Functions on consumption plan saves money as the process runs only when a bike is returned.
- **Integrations:** Closer integration with Logic Apps is crucial. Azure Functions offer better integration and control from Logic Apps visual designer.

## Conclusion

Opting for Azure Functions aligns with the need for a code-first approach, cost-effectiveness, and seamless integration with the existing Logic App for bike booking and rental process. This choice ensures efficient management of the bike maintenance workflow while maintaining flexibility for future enhancements.

---
