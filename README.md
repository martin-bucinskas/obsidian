# Obsidian - solid infrastructure for your needs

Obsidian is an automation suite to help standardise, manage and track everything infrastructure.

## How does it work

Obsidian uses configurations written in TOML. These configurations live in shards.

### Shard

A shard is a component or a group of components that achieve a function.

For example, accounts is a shard which will have a TOML configuration for managing accounts in your AWS/GCP/Azure system.

You can create your own shards with the help of Pulumi.

## Structure

Obsidian follows a simple structure that allows easy management.

```
 .
 |__ obsidian
 |__ shards
 |   |__ accounts.toml
 |__ .diff
 |   |_ accounts.toml
 |
 | settings.toml
 | obsidian.js
 ```

**obsidian** contains the code for obsidian.
**shards** contains the shards with their configurations.
**.diff** contains the diff file for each shard.
**settings.toml** is used to preconfigure obsidian.
**obsidian.js** is the entry point.
