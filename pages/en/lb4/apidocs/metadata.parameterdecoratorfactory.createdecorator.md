---
lang: en
title: 'API docs: metadata.parameterdecoratorfactory.createdecorator'
keywords: LoopBack 4.0, LoopBack 4
sidebar: lb4_sidebar
editurl: https://github.com/strongloop/loopback-next/tree/master/packages/metadata
permalink: /doc/en/lb4/apidocs.metadata.parameterdecoratorfactory.createdecorator.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/metadata](./metadata.md) &gt; [ParameterDecoratorFactory](./metadata.parameterdecoratorfactory.md) &gt; [createDecorator](./metadata.parameterdecoratorfactory.createdecorator.md)

## ParameterDecoratorFactory.createDecorator() method

Create a parameter decorator function

<b>Signature:</b>

```typescript
static createDecorator<T>(key: MetadataKey<T, ParameterDecorator>, spec: T, options?: DecoratorOptions): ParameterDecorator;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  key | [MetadataKey](./metadata.metadatakey.md)<!-- -->&lt;T, ParameterDecorator&gt; | Metadata key |
|  spec | T | Metadata object from the decorator function |
|  options | [DecoratorOptions](./metadata.decoratoroptions.md) | Options for the decorator |

<b>Returns:</b>

ParameterDecorator


