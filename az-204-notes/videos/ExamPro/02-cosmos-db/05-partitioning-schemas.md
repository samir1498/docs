# Partitioning Schemas in Cosmos DB

## Introduction

Partitioning schemas play a pivotal role in Azure Cosmos DB, especially concerning scalability in New SQL databases.

## Partition Keys

- Key for grouping items within Cosmos DB, analogous to primary keys in traditional relational databases.

## Logical Partition

- Group of items sharing identical partition key values, managed by Azure Cosmos DB.

## Physical Partitions

- Sets of logical partitions managed by Azure Cosmos DB, possibly with one-to-many relationships.

## Replica Sets

- Groups of physical partitions representing dynamically balanced replicas spanning multiple fault domains for enhanced redundancy and reliability.
