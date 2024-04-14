# Choosing the Best Design-First Technology for Bike Rental Process Automation

## Scenario Overview

In this scenario, you aim to automate and modernize the bike booking process for your rental business, integrating bike tracking technology across campuses. The process involves customer requests, bike availability checks, location tracking, and rental management.

## Business Process Workflow

- Customer requests a bike, providing details.
- Shop staff record customer details and bike specifications.
- Check bike availability based on features and frame size.
- Reserve/book the bike if available, else find the nearest one.
- Notify staff to move the bike and update location.
- Scan barcode at new location, rent out the bike, and process payment.

## Technology Options

You have the following Azure technologies to implement the workflow and integrate with the bike location database:

1. **Microsoft Power Automate**
2. **Azure Logic Apps**
3. **Azure Functions**
4. **Azure App Service WebJobs**

## Decision Criteria

### Design-first or code-first?

- **Preference:** Design-first *(Managing Director and her staff want to understand the workflow at a higher level than examining the code and implementation)* to visualize and maintain the workflow easily.
- **Technology Choice:** Azure Logic Apps or Microsoft Power Automate.

### Microsoft Power Automate or Azure Logic Apps?

- **Requirement:** Develop a custom connector for the bike location database.
- **Choice:** Azure Logic Apps for seamless connector development and workflow creation by developers.

## Conclusion

Choosing Azure Logic Apps aligns with the requirement for a design-first approach and developer involvement in creating custom connectors. This ensures clarity, maintainability, and efficient integration of the bike rental process with the tracking system.
