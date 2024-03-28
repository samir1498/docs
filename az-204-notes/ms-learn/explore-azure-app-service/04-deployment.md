# Deploying to Azure App Service

**Overview:**
Azure App Service supports both automated and manual deployment methods, providing flexibility for development teams to implement efficient deployment pipelines tailored to their unique requirements.

**Automated Deployment:**
Automated deployment, also known as continuous deployment, enables the rapid and repetitive delivery of new features and bug fixes with minimal disruption to end users. Azure App Service offers automated deployment directly from various sources:

1. **Azure DevOps Services:**
   - Push code to Azure DevOps Services, where it undergoes cloud-based build, test, and release processes before deployment to an Azure Web App.

2. **GitHub:**
   - Connect your GitHub repository to Azure for seamless automated deployment. Changes pushed to the production branch trigger automatic deployment to Azure Web App.

3. **Bitbucket:**
   - Similar to GitHub, Bitbucket integration allows for automated deployment directly from the repository.

**Manual Deployment:**
For situations requiring manual intervention or alternative deployment methods, Azure App Service provides several options:

1. **Git:**
   - Utilize the Git URL provided by App Service to add a remote repository and push code changes, triggering app deployment.

2. **CLI (Command-Line Interface):**
   - Use the `webapp up` feature of the `az` command-line interface to package and deploy the app. This method can also create a new App Service web app if one doesn't exist.

3. **Zip Deploy:**
   - Send a ZIP file containing application files to App Service using tools like curl or similar HTTP utilities.

4. **FTP/S (File Transfer Protocol/Secure):**
   - Traditional FTP or FTPS can be used to manually upload code to App Service, providing an alternative deployment option.

**Utilizing Deployment Slots:**
When deploying new production builds, it's advisable to leverage deployment slots for improved deployment management and minimal downtime:

- **Deployment Slots:**
  - In the Standard App Service Plan tier or higher, deploy apps to staging environments using deployment slots.
  - Swap staging and production slots to seamlessly transition to the new build, warming up necessary worker instances to match production scale and eliminating downtime.

Azure App Service's deployment options cater to diverse deployment needs, ensuring efficient and reliable delivery of web applications.
