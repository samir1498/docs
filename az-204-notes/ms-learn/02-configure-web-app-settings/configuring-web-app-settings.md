# Configuring Web App Settings and Connection Strings in Azure App Service

## Introduction

In Azure App Service, configuring app settings and connection strings is crucial for managing your web application's environment variables and database connections securely. This document provides a comprehensive guide on how to configure these settings using the Azure Portal.

## App Settings Configuration

### Accessing Application Settings

1. Navigate to your app's management page in the Azure Portal.
2. Select **Configuration > Application Settings**.

### Adding and Editing App Settings

- To add a new app setting:
  - Click on **New application setting**.
  - Specify the setting name and value.
  - Optionally, specify if the setting is swappable for deployment slots.
  - Stick the setting to the current slot if applicable.
- To edit an existing app setting:
  - Modify the value as needed.
- Click **Update** when finished, and remember to **Save** on the Configuration page.

### Bulk Editing of App Settings

- Click on **Advanced edit** to add or edit app settings in bulk.
- Ensure the JSON formatting is correct:

```json
[
  {
    "name": "<key-1>",
    "value": "<value-1>",
    "slotSetting": false
  },
  {
    "name": "<key-2>",
    "value": "<value-2>",
    "slotSetting": false
  },
  ...
]
```

### Note for Linux Containers

- Ensure correct configuration for nested JSON key structures in app setting names.

## Connection Strings Configuration

### Overview

- Connection strings are crucial for database connectivity.
- Always use connection strings for non-.NET languages.
- Connection strings are encrypted-at-rest for security.

### Adding and Editing Connection Strings

- Follow similar principles as app settings for adding and editing.
- Connection strings can also be tied to deployment slots.
- Use appropriate JSON formatting:

```json
[
  {
    "name": "name-1",
    "value": "conn-string-1",
    "type": "SQLServer",
    "slotSetting": false
  },
  {
    "name": "name-2",
    "value": "conn-string-2",
    "type": "PostgreSQL",
    "slotSetting": false
  },
  ...
]
```

## Conclusion

Proper configuration of app settings and connection strings in Azure App Service ensures your web application runs smoothly, securely, and efficiently. Follow the guidelines provided in this document for seamless management of your application's environment variables and database connections.
