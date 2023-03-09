---
outline: deep
---

# Schema Overview

<Badges>

[![npm version](https://img.shields.io/npm/v/@feathersjs/schema.svg?style=flat-square)](https://www.npmjs.com/package/@feathersjs/schema)
[![Changelog](https://img.shields.io/badge/changelog-.md-blue.svg?style=flat-square)](https://github.com/feathersjs/feathers/blob/dove/packages/schema/CHANGELOG.md)

</Badges>

`@feathersjs/schema` offers a way to define data models and dynamically resolve them. It consists of three main components:

1.  [JSON schema](https://json-schema.org/) which can be defined using [TypeBox](./typebox.md) or [plain JSON schema](./schema.md).  This defines a data model with TypeScript types and validations. Advantages of this include:
  - Automatic generation of TypeScript types from schema definitions
  - Automatic generation of API documentation
  - Creation of [database adapter](../databases/common.md) models without duplicating the data format
2.  [Validators](./validators.md), which use a [TypeBox](./typebox.md) or [JSON](./schema.md) TypeBox or JSON schema to validate data. Benefits include:
  - Ensuring data is valid and in the correct format
  - Validating query string queries and converting them to the correct type
3.  [Resolvers](./resolvers.md), which resolve properties based on a context (usually the [hook context](../hooks.md)). These can be used for various purposes, such as:
  - Adding default and computed values
  - Populating associations
  - Securing queries and limiting requests to a user
  - Removing protected properties for external requests
  - Adding read and write permissions on the property level
  - Hashing passwords and validating dynamic password policies
