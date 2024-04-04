# Creating a Static HTML Web App Using Azure Cloud Shell

**Duration:** 15 minutes

**Objective:**
In this exercise, you'll deploy a basic HTML+CSS site to Azure App Service using the Azure CLI `az webapp up` command. You'll then update the code and redeploy it using the same command.

**Steps:**

1. **Download Sample App:**
   - Create a directory and navigate to it in the Azure Cloud Shell.

     ```bash
     mkdir htmlapp
     cd htmlapp
     ```

   - Clone the sample app repository to your `htmlapp` directory using Git.

     ```bash
     git clone https://github.com/Azure-Samples/html-docs-hello-world.git
     ```

   - Set variables to hold the resource group and app names.

     ```bash
     resourceGroup=$(az group list --query "[].{id:name}" -o tsv)
     appName=az204app$RANDOM
     ```

2. **Create the Web App:**
   - Change to the directory containing the sample code and run the `az webapp up` command.

     ```bash
     cd html-docs-hello-world
     az webapp up -g $resourceGroup -n $appName --html
     ```

   - Wait for the command to complete. It will display information including the app URL.

3. **Verify the App:**
   - Open a new browser tab and navigate to the app URL.
   - Verify that the app is running, noting the title at the top of the page.

4. **Update and Redeploy the App:**
   - Type `code index.html` in the Cloud Shell to open the editor.
   - Change the text within the `<h1>` heading tag.
   - Save and exit the editor (Ctrl + S, Ctrl + Q).
   - Redeploy the app using the same `az webapp up` command.

     ```bash
     az webapp up -g $resourceGroup -n $appName --html
     ```

   - Once deployment is completed, refresh the browser tab to see the updated content.

**Note:** Ensure you have selected a region from the provided list before creating resources.
