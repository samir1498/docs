# Configuring Path Mappings in Azure App Service

## Introduction

In the Configuration > Path mappings section of Azure App Service, you can customize handler mappings, virtual applications, and directories. This document provides a detailed guide on configuring path mappings based on the OS type of your app.

## Windows Apps (Uncontainerized)

- **Description**: Allows you to add custom script processors to handle requests for specific file extensions.
- **Adding a Custom Handler**:
  - Click on **New handler**.
  - Configure the handler with the following details:
    - Extension: File extension to handle (e.g., \*.php or handler.fcgi).
    - Script processor: Absolute path of the script processor (use D:\home\site\wwwroot to refer to the app's root directory).
    - Arguments: Optional command-line arguments for the script processor.

### Virtual Applications and Directories

- **Description**: Lets you configure virtual applications and directories.
- **Configuration**:
  - Specify each virtual directory and its corresponding physical path relative to the website root (D:\home).
  - To mark a virtual directory as a web application, clear the Directory checkbox.

## Linux and Containerized Apps

### Custom Storage Configuration

- **Description**: Allows addition of custom storage for containerized apps, including Linux apps and Windows/Linux custom containers.
- **Adding Azure Storage Mount**:
  - Click on **New Azure Storage Mount**.
  - Configure the custom storage with the following details:
    - Name: Display name.
    - Configuration options: Basic or Advanced.
    - Storage accounts: Select the storage account with the container.
    - Storage type: Azure Blobs or Azure Files (Windows container apps support Azure Files only).
    - Storage container: For basic configuration, specify the container.
    - Share name: For advanced configuration, provide the file share name.
    - Access key: For advanced configuration, enter the access key.
    - Mount path: Absolute path in the container to mount the custom storage.

## Conclusion

Configuring path mappings in Azure App Service allows you to customize handler mappings and manage virtual applications, directories, and custom storage effectively based on your application's requirements and OS type. Follow the guidelines provided in this document for seamless configuration of path mappings in your Azure App Service environment.
