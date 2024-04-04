# Choosing a Partition Key in Azure Cosmos DB

## Partition Key Composition

A partition key consists of two components: the partition key path and the partition key value.

## Partition Key Path

Partition key path is determined based on the unique identifier for the item. For instance, a user ID in the given example would be represented as `/userId`. The path follows a standard notation.

## Acceptable Characters

Partition key paths can include numerical or underscore characters and support nested objects using the forward slash notation.

## Partition Key Value

The partition key value can be either a string or numeric type. In the example provided, it's a string, such as `"userId"`.

## Choosing the Right Partition Key

- It should be a property with a value that doesn't change.
- It should have a wide range of possible values to ensure even Request Unit (RU) consumption and storage distribution across physical partitions.
