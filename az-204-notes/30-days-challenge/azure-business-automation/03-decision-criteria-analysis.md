# Azure Service Options for Business Process Automation

## Decision Criteria

### Design-First vs. Code-First

#### Design-First Approach

- **Logic Apps:** Intuitive visual designer, suitable for users with development skills.
- **Microsoft Power Automate:** User-friendly interface, ideal for non-coders, limited source code access.

#### Code-First Approach

- **WebJobs:** Granular control, suitable for existing Azure applications, C# on Windows only.
- **Azure Functions:** Serverless, scalable, supports multiple languages, pay-per-use model.

### Mix & Match

- **Flexibility:** No requirement for uniformity, mix technologies based on requirements.
- **Interoperability:** Call one workflow from another, enhancing modularity and reuse.
- **Example:** Implement Power Automate section and call it from Logic Apps, WebJobs, or Functions for seamless integration.

---
