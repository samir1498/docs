# Summary

In Azure, a function only runs when something explicitly tells it to execute. In this module, we explored the timer, HTTP, and Blob storage triggers.

These three triggers are common triggers you can use to define your functions. Azure Functions provides a wide selection of both triggers and bindings that you can use to connect your function code to Azure services and other partner services. Although each trigger type has specific requirements, the implementation and usage patterns are similar.

## Clean up

The sandbox automatically cleans up your resources when you're finished with this module.

When you're working in your own subscription, it's a good idea at the end of a project to identify whether you still need the resources you created. Resources that you leave running can cost you money. You can delete resources individually or delete the resource group to delete the entire set of resources.

## Check your knowledge

1. **A CRON expression is a string that consists of six fields that represent a set of times. The order of the six fields in Azure is: {second} {minute} {hour} {day} {month} {day of the week}. Suppose you needed a CRON expression that meant "every day", what special character would you put in the {day of the week} position?**

   - `*`

   An asterisk specifies that every possible value should be selected. Having an asterisk in the {day of the week} field means that every day should be selected.

2. **Suppose your Azure Function has a blob trigger associated with it and you want it to execute only when png images are uploaded. Which of the following blob trigger Path values should you use?**

   - `samples-workitems/{name}.png`

   The Path tells the blob trigger where it should monitor for changes, and if there are any filters applied. Adding a file extension to the Path specifies that uploaded files must have that file extension in order for the trigger to invoke the function.

3. **True or false: an Azure Function can have multiple triggers associated with it?**

   - False

   Every Azure Function must have exactly one trigger associated with it. If you want to use multiple triggers, you must create multiple functions.
