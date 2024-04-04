# Choosing a Unique Key

## Overview

Unique keys in Azure Cosmos DB provide developers with the ability to add a layer of data integrity to their database. This ensures the uniqueness of one or more values per partition key, thereby preventing duplicate entries within logical partitions.

## Key Considerations

- Unique keys are scoped to a logical partition, ensuring uniqueness within that partition.
- Planning is crucial as existing containers cannot update to use a different unique key. It must be chosen during the initial creation process.
- Unique key policies can include a maximum of 16 path values and 10 unique key constraints or combinations.

## Implementation Details

- Unique keys aren't case-sensitive, providing flexibility in key selection.
- When a container has a unique key policy, the request units (RU) charged for create, update, and delete operations are slightly higher.

## Example

If, for instance, a container is partitioned based on zip codes, the unique key could be based on a combination of first name and address zip to ensure the uniqueness of entries.

## Limitations

- Existing containers cannot be updated to use a different unique key.
- Unique keys policies can include a maximum of 16 path values and 10 unique key constraints or combinations.
