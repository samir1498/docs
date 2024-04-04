# Exploring Authentication and Authorization in Azure App Service

**Overview:**
Azure App Service offers built-in authentication and authorization support, streamlining the process of signing in users and accessing data for web apps, RESTful APIs, mobile back ends, and Azure Functions.

**Why Use Built-in Authentication?**

- Saves time and effort by providing out-of-the-box authentication with federated identity providers.
- Allows integration with various authentication capabilities without the need for extensive code implementation.
- Supports multiple login providers such as Microsoft identity platform, Facebook, Google, Twitter, GitHub, and any OpenID Connect provider.

**Identity Providers:**

- App Service uses federated identity, wherein third-party identity providers manage user identities and authentication flow.

**How It Works:**

- The authentication and authorization module operates within the same sandbox as your application code, intercepting every incoming HTTP request before it reaches your application logic.
- It handles several key tasks:
  - Authenticating users and clients with specified identity providers.
  - Validating, storing, and refreshing OAuth tokens issued by the configured identity providers.
  - Managing authenticated sessions.
  - Injecting identity information into HTTP request headers.
- This module runs separately from your application code and can be configured either through Azure Resource Manager settings or a configuration file.
- Notably, in Linux and container environments, this module operates in a separate container, isolated from your application code due to its out-of-process nature. As a result, direct integration with specific language frameworks is not feasible in these environments.
- Authentication flow differs depending on the presence of a provider SDK:
  - Without a provider SDK, the application delegates federated sign-in to App Service, managing the sign-in process on the server side (server-directed flow).
  - With a provider SDK, the application manually signs users in to the provider and submits the authentication token to App Service for validation (client-directed flow). This applies to REST APIs, Azure Functions, JavaScript browser clients, and native mobile apps using the provider's SDK.

**Authorization Behavior:**

- Configurable options include allowing unauthenticated requests or requiring authentication.
- For unauthenticated requests, authorization can be deferred to application code or rejected with redirect actions or HTTP status codes.

**Token Store:**

- Azure App Service provides a built-in token store, serving as a repository of tokens associated with users of web apps, APIs, or native mobile apps.
- Tokens store are immediately available upon enabling authentication with any provider.

**Logging and Tracing:**

- Authentication and authorization traces are collected in application logs when application logging is enabled.
- Facilitates troubleshooting authentication errors by providing detailed information in existing application logs.
