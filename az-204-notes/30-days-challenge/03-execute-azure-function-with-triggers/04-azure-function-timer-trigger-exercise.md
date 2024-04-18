# Exercise - Create a Timer Trigger

## Verify your account

In this unit, we'll create an Azure Function app that's invoked every 20 seconds using a timer trigger.

## Create an Azure Function App

1. Sign in to the Azure portal using the same account you used to activate the sandbox.
2. Under Azure services, select Create a resource.
3. Select Web, then Function App from the results.
4. On the Basics tab, fill in the necessary details such as Subscription, Resource Group, Function App name, Runtime stack, Version, Region, Operating System, and Plan type.
5. Select Next: Storage, and fill in the required details for Storage.
6. Select Review + create to validate your input, and then select Create.

## Create and Configure a Timer-Triggered Function

1. In the Function App menu, select the Functions tab.
2. Select the Create in Azure portal button.
3. Under Select a template, choose Timer trigger.
4. Enter `*/20 * * * * *` in the Schedule field, then select Create.

## Test the Timer

1. On the TimerTrigger1 pane, select Code + Test under Developer.
2. Select App Insight Logs drop-down, then select Filesystem Logs.
3. Observe the log pane for a new message arriving every 20 seconds.
4. To stop the function, select Stop in the Logs pane command bar.
5. To disable the function, go to TimerTrigger1 menu, select Overview, then choose Disable in the command bar.

## Next unit:  Execute an Azure function with an HTTP request
