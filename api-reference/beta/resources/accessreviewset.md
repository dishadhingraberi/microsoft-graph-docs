---
title: "accessReviewSet resource type"
description: "Container for the base resources that expose the access reviews API and features. Currently exposes only the accessReviewScheduleDefinition resource."
author: "zhusijia26"
ms.localizationpriority: medium
ms.prod: "governance"
doc_type: resourcePageType
---

# accessReviewSet resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Container for the base resources that expose the access reviews API and features. Currently exposes only the [accessReviewScheduleDefinition](../resources/accessreviewscheduledefinition.md) relationship.

Inherits from [entity](entity.md).

## Methods

None.

## Properties

None.

## Relationships

|Relationship|Type|Description|
|:---|:---|:---|
|decisions|[accessReviewInstanceDecisionItem](../resources/accessreviewinstancedecisionitem.md) collection| Represents an Azure AD access review decision on an instance of a review.|
|definitions|[accessReviewScheduleDefinition](../resources/accessreviewscheduledefinition.md) collection| Represents the template and scheduling for an access review. |
|historyDefinitions|[accessReviewHistoryDefinition](../resources/accessreviewhistorydefinition.md) collection| Represents a collection of access review history data and the scopes used to collect that data.|
|policy|[accessReviewPolicy](../resources/accessreviewpolicy.md)| Resource that enables administrators to manage directory-level access review policies in their tenant.|

## JSON representation

The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.accessReviewSet",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.accessReviewSet"
}
```

