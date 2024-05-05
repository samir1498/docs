# Exercise - Publish a function to Azure using Core Tools

## Create a function app

1. **Create a function app in Azure**:
   - Use Azure CLI commands to create a function app in Azure. Run the following commands in Azure Cloud Shell:

     ```bash
     RESOURCEGROUP="learn-5ec19e9d-712c-461f-b1c0-6dada83eb975"
     STORAGEACCT=learnstorage$(openssl rand -hex 5)
     FUNCTIONAPP=learnfunctions$(openssl rand -hex 5)

     az storage account create \
       --resource-group "$RESOURCEGROUP" \
       --name "$STORAGEACCT" \
       --kind StorageV2 \
       --location centralus

     az functionapp create \
       --resource-group "$RESOURCEGROUP" \
       --name "$FUNCTIONAPP" \
       --storage-account "$STORAGEACCT" \
       --runtime node \
       --consumption-plan-location centralus \
       --functions-version 4
     ```

## Publish to Azure

2. **Publish your functions project**:
   - Navigate to the functions project folder in Cloud Shell using `cd ~/loan-wizard`.
   - Run the command `func azure functionapp publish "$FUNCTIONAPP" --force` to publish your project to the specified function app in Azure.
   - Replace `$FUNCTIONAPP` with the name of your target function app in Azure.
   - Append `--force` to update the function app version mismatch if encountered.
   - If the command displays an error that it can't find your app, wait two minutes and try again. New function apps take a few seconds to become discoverable by the Core Tools after creation.

3. **Run the function**:
   - Retrieve the request URL by running the command `func azure functionapp list-functions "$FUNCTIONAPP" --show-keys`.
   - Paste the URL from the output into a new browser tab to access your function. No keys are included in the output due to an anonymous authorization level.
   - Add `?principal=5000&rate=.035&term=36` to the end of the URL and press Enter to execute the function. The expected result returned should be `6300.000000000001`.
