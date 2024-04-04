# Authorization Levels in Azure Functions (AZ 204)

**Overview:**
Authorization levels in Azure Functions play a vital role in managing access and security when invoking functions. This document provides an overview of the three authorization levels available and instructions for modifying them as needed.

## Authorization Levels

1. **Anonymous:**
   - Allows anyone to invoke the function without requiring any key.
   - Suitable for scenarios where broad access is permissible, such as public APIs with no sensitive data.

2. **Function:**
   - Requires a specified API key for invocation.
   - Default setting for functions, providing a balance between security and accessibility.
   - Recommended for most use cases where controlled access is necessary.

3. **Admin:**
   - Requires the use of a master key for invocation.
   - Provides the highest level of security and control over function access.
   - Typically reserved for administrative tasks or functions handling sensitive data.

**Changing Authorization Levels:**

- To modify authorization levels after deployment:
  - Navigate to the Azure portal.
  - Click on the HTTPS trigger associated with the function.
  - Adjust the authorization level as needed.
- Note: Certain runtime configurations may limit the ability to change authorization levels via the portal.
