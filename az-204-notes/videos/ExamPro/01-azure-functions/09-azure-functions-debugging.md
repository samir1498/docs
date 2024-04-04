# Azure Functions Debugging

## Overview

This document serves as a concise guide for understanding Azure Functions debugging, a crucial aspect covered in the AZ-204 certification exam offered by Microsoft. We'll explore the process of enabling streaming logs, essential for effective error detection and resolution.

## Key Insights

### 1. Activation of Streaming Logs

- Begin Azure Functions debugging by activating streaming logs.
- Streaming logs provide real-time visibility into Azure Functions, facilitating swift error identification.

### 2. Available Options

- Two primary options for streaming logs include:
  - **Built-in Logging Stream:** Access application log files within the app service platform.
  - **Live Metrics Stream:** Access real-time log data and metrics for function apps connected to Application Insights.

### 3. Accessibility

- Log streams can be accessed through:
  - **Azure Portal:** Centralized platform for monitoring and managing Azure resources.
  - **Local Developer Environments:** Utilize tools like Visual Studio Code for debugging during development.

### 4. Considerations

- Hosting location may affect real-time log availability.
- Ensure the function app is hosted on an appropriate platform to maximize the benefits of streaming logs.
