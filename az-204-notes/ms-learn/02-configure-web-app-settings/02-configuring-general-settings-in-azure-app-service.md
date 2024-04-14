# Configuring General Settings in Azure App Service

## Introduction

In the Configuration > General settings section of Azure App Service, you can configure various common settings for your application. This document provides an overview of the available settings and their functionalities.

## Stack Settings

- **Description**: Defines the software stack to run the app, including the language and SDK versions.
- **Note**: For Linux apps and custom container apps, you can also set an optional start-up command or file.

## Platform Settings

- **Bitness**: Specifies whether the platform runs in 32-bit or 64-bit mode.
- **WebSocket Protocol**: Enables WebSocket protocol support, beneficial for ASP.NET SignalR or socket.io applications.
- **Always On**: Keeps the app loaded even during periods of no traffic, essential for continuous WebJobs or those triggered using a CRON expression.
- **Managed Pipeline Version**: Sets the IIS pipeline mode; choose Classic for legacy apps requiring an older version of IIS.
- **HTTP Version**: Enables support for HTTP/2 protocol by setting it to 2.0.
- **ARR (Application Request Routing) Affinity**: Controls client routing in a multi-instance deployment, ensuring the client remains routed to the same instance for the duration of the session. Can be turned off for stateless applications.
- **Debugging**: Enables remote debugging for ASP.NET, ASP.NET Core, or Node.js apps. Automatically turns off after 48 hours.
- **Incoming Client Certificates**: Enforces the requirement for client certificates in mutual authentication, restricting access to your app by enabling different types of authentication.

## Conclusion

Configuring general settings in Azure App Service allows you to tailor your application environment according to your specific requirements. By understanding and utilizing these settings effectively, you can enhance the performance, security, and reliability of your web applications deployed on Azure App Service.
