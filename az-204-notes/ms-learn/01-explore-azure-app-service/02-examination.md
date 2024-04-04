# Exploring Azure App Service

## Overview

Azure App Service is an HTTP-based service for hosting web applications, REST APIs, and mobile back ends. It supports various programming languages and frameworks, running on both Windows and Linux environments.

## Key Features

1. **Auto Scale Support:**
   - Built-in scaling capabilities enable adjustment of resources based on application usage.
   - Scaling can be done by changing the number of cores or RAM, and by increasing or decreasing machine instances.

2. **Continuous Integration/Deployment (CI/CD) Support:**
   - Azure App Service integrates with Azure DevOps Services, GitHub, Bitbucket, FTP, and local Git repositories for automated code syncing.

3. **Deployment Slots:**
   - Separate deployment slots allow testing and staging of app changes before production deployment.
   - Slots have unique host names and content/configurations can be swapped easily.

4. **App Service on Linux:**
   - Supports hosting web apps natively on Linux and running custom Linux containers.
   - Built-in images available for popular languages like Node.js, Java, PHP, Python, .NET, and Ruby.

## Limitations

- App Service on Linux:
  - Not supported on the Shared pricing tier.
  - Azure portal displays only features currently compatible with Linux apps.
  - Deployed code/content may have higher disk latency when using built-in images.
