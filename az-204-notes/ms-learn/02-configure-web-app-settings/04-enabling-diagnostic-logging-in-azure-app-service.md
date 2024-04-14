# Enabling Diagnostic Logging in Azure App Service

## Introduction

Diagnostic logging in Azure App Service assists with debugging by providing insights into the behavior of your application. This document outlines how to enable diagnostic logging, configure log storage, add instrumentation to your application, and access logged information in Azure.

## Enable Application Logging (Windows)

1. Navigate to your app in the Azure portal and select **App Service logs**.
2. Enable either **Application Logging (Filesystem)** or **Application Logging (Blob)**, or both.
   - Filesystem: For temporary debugging (turns off after 12 hours).
   - Blob: For long-term logging (requires a blob storage container).
3. Configure the **Level of details** included in the logs based on the desired categories.

## Enable Application Logging (Linux/Container)

1. Set the **Application logging** option to **File System** in App Service logs.
2. Specify disk quota in **Quota (MB)** and set the **Retention Period (Days)** for log retention.
3. Click **Save** when finished.

## Enable Web Server Logging

1. Select either **Storage** or **File System** to store web server logs.
2. Set the **Retention Period (Days)** for log retention.
3. Click **Save**.

## Adding Log Messages in Code

- Use standard logging facilities in your application code to send log messages to the application logs.
  - ASP.NET: Utilize `System.Diagnostics.Trace` class.
  - ASP.NET Core: Use `Microsoft.Extensions.Logging.AzureAppServices` logging provider.
  - Python: Employ the OpenCensus package.

## Stream Logs

- Before streaming logs, enable the desired log type.
- Azure Portal: Navigate to your app and select **Log stream**.
- Azure CLI: Use `az webapp log tail` command.
- Local Console: Install Azure CLI, sign in, and follow the instructions shown for Azure CLI.

## Access Log Files

- For logs stored in Azure Storage blobs, use a client tool compatible with Azure Storage.
- For logs stored in the App Service file system, download the ZIP file from:
  - Linux/Container Apps: `https://<app-name>.scm.azurewebsites.net/api/logs/docker/zip`
  - Windows Apps: `https://<app-name>.scm.azurewebsites.net/api/dump`

## Conclusion

Enabling diagnostic logging in Azure App Service provides valuable insights into your application's behavior and aids in debugging. By following the steps outlined in this document, you can configure logging settings, add instrumentation, and access logged information effectively.
