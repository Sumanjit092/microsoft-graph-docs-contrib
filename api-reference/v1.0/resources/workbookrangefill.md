---
title: "workbookRangeFill resource type"
description: "Represents the background of a range object."
author: "lumine2008"
ms.localizationpriority: medium
ms.subservice: "excel"
doc_type: resourcePageType
---

# workbookRangeFill resource type

Namespace: microsoft.graph

Represents the background of a range object.


## Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get RangeFill](../api/rangefill-get.md) | [workbookRangeFill](workbookrangefill.md) |Read properties and relationships of rangeFill object.|
|[Update](../api/rangefill-update.md) | [workbookRangeFill](workbookrangefill.md)	|Update RangeFill object. |
|[Clear](../api/rangefill-clear.md)|None|Resets the range background.|

## Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|color|string|HTML color code representing the color of the border line, of the form #RRGGBB (for example "FFA500") or as a named HTML color (for example "orange")|

## Relationships
None


## JSON representation

The following JSON representation shows the resource type.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookRangeFill"
}-->

```json
{
  "color": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeFill resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

