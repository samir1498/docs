# Exercise - Create a Blob Trigger

In this unit, we're going to create an Azure function that displays the name and size of a blob when it's created or updated.

## Create a Blob Trigger

1. Open the Azure portal and sign in with the same account you used to activate the sandbox.
2. In the All resources pane, select your Function App.
3. On the Functions tab, click the Create button at the top.
4. Select Azure Blob Storage trigger from the list of templates.
5. Accept the default function name and storage account connection.
6. Click Create to create the function.

## Create a Blob Container

Let's create a blob container in Storage Browser to trigger the blob trigger.

1. In the Azure portal, go to your storage account.
2. Click Blobs and then Containers.
3. Click + Container to create a container named "samples-workitems".

## Turn on Your Blob Trigger

Now that we've created our container to monitor, let's run our function so we can see output when a blob is created.

1. Switch back to the browser tab with your Azure Function (or reopen it).
2. Select your blob trigger in the Functions tab in the center of the screen. In the left menu pane, under Developer, select Code + Test.
3. Expand the Logs tab at the bottom of the screen if necessary.
4. Select the App Insight Logs drop-down, and then select Filesystem Logs. Select OK when the Switching to filesystem based logs... message displays.

## Create a Blob

Our blob trigger is now up and listening for activity. Let's create a blob to see if we get a log message.

1. Switch back to the browser tab with Storage Browser.
2. In Storage Browser, select the samples-workitems container from the Blob containers list.
3. In the Authentication method: link at the top if the list, select Switch to Access key.
4. In the top menu bar, select Upload. The Upload blob pane opens.
5. From the Files field, select any file from your computer.
6. Select Upload.

Switch back to the Azure Function tab and check the logs. Your blob trigger should execute automatically when you upload a file.

## Next unit: Summary
