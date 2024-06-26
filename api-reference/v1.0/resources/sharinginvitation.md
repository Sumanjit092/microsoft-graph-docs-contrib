---
author: spgraph-docs-team
ms.date: 09/10/2017
title: sharingInvitation resource type
ms.localizationpriority: medium
description: "The sharingInvitation resource groups invitation-related data items into a single structure."
ms.subservice: onedrive
doc_type: resourcePageType
---

# sharingInvitation resource type

Namespace: microsoft.graph

Groups invitation-related data items into a single structure.

## JSON representation

The following JSON representation shows the resource type.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.sharingInvitation"
}-->

```json
{
  "email": "string",
  "invitedBy": {"@odata.type": "microsoft.graph.identitySet" },
  "signInRequired": true
}
```

## Properties

| Property Name  | Type            | Description
|:---------------|:----------------|:------------------------------------------
| email          | String          | The email address provided for the recipient of the sharing invitation. Read-only.
| invitedBy      | [identitySet][] | Provides information about who sent the invitation that created this permission, if that information is available. Read-only.
| signInRequired | Boolean         | If `true` the recipient of the invitation needs to sign in in order to access the shared item. Read-only.

## Remarks

For more information about the facets on a **driveItem**, see [driveItem](driveitem.md).

[DriveItem]: driveitem.md
[IdentitySet]: identityset.md

<!-- {
  "type": "#page.annotation",
  "description": "The sharing invitation facet describes details of a sharing invitation associated with a permission.",
  "keywords": "image,width,height,item,facet",
  "section": "documentation",
  "tocPath": "Facets/SharingInvitation"
} -->

