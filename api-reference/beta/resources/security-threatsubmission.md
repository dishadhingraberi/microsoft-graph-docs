---
title: "threatSubmission resource type"
description: "Represents a threat submission, which is used to submit suspected email, UTL, or file threats to Microsoft Defender."
author: "caigen"
ms.localizationpriority: medium
ms.prod: "security"
doc_type: resourcePageType
---

# threatSubmission resource type

Namespace: microsoft.graph.security

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a threat submission, which is an abstract type for representing suspected spam, malware, phish, and blocked legitimate emails; malware, phish and blocked legitimate URLs; phish, malware and blocked legitimate email attachments to Microsoft Defender for Office 365, and suspicious files to Microsoft Defender for Endpoint.

This resource can also be used to submit false positive cases that should not be blocked by Microsoft Defender for Office 365; for example, not junk emails, safe URLs, and safe email attachments.

This is an abstract type. Inherits from [entity](../resources/entity.md). Base type of [emailThreatSubmission](../resources/security-emailthreatsubmission.md), [urlThreatSubmission](../resources/security-urlthreatsubmission.md), [fileThreatSubmissin](../resources/security-filethreatsubmission.md).

## Properties
| Property        | Type                       | Description                                                                      |
|:----------------|:---------------------------|:---------------------------------------------------------------------------------|
| adminReview     | [security.submissionAdminReview](../resources/security-submissionadminreview.md)| Specifies the admin review property which constitutes of who reviewed the user submission, when and what was it identified as. |
| category        | submissionCategory         | Specifies the category of the submission. Supports `$filter = category eq 'value'`. The possible values are: `notJunk`, `spam`, `phishing`, `malware` and `unkownFutureValue`.|
| clientSource    | submissionClientSource     | Specifies the source of the submission. The possible values are: `microsoft`,  `other` and `unkownFutureValue`. |
| contentType     | submissionContentType      | Specifies the type of content being submitted. The possible values are: `email`, `url`, `file`, `app` and `unkownFutureValue`.  |
| createdBy       | [security.submissionUserIdentity](../resources/security-submissionuseridentity.md)     | Specifies who submitted the email as a threat. Supports `$filter = createdBy/email eq 'value'`. |
| createdDateTime | DateTimeOffset  | Specifies when the threat submission was created. Supports `$filter = createdDateTime ge 2022-01-01T00:00:00Z and createdDateTime lt 2022-01-02T00:00:00Z`.             |
| id              | String                     | Specifies the ID of threat submission. |
| result          | [security.submissionResult](../resources/security-submissionresult.md)          | Specifies the result of the analysis performed by Microsoft.  |
| source          | submissionSource           | Specifies the role of the submitter. Supports `$filter = source eq 'value'`. The possible values are: `administrator`,  `user` and `unkownFutureValue`.  |
| status          | longRunningOperationStatus | Indicates whether the threat submission has been analyzed by Microsoft. Supports `$filter = status eq 'value'`. The possible values are: `notStarted`, `running`, `succeeded`, `failed`, `skipped` and `unkownFutureValue`. |
| tenantId        | String                     | Indicates the tenant id of the submitter. Not required when created using a `POST` operation. It is extracted from the token of the post API call. |

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.security.threatSubmission",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.security.threatSubmission",
  "id": "String (identifier)",
  "tenantId": "String",
  "createdDateTime": "String (timestamp)",
  "contentType": "String",
  "category": "String",
  "source": "String",
  "createdBy": {
    "@odata.type": "microsoft.graph.security.submissionUserIdentity"
  },
  "status": "String",
  "result": {
    "@odata.type": "microsoft.graph.security.submissionResult"
  },
  "adminReview": {
    "@odata.type": "microsoft.graph.security.submissionAdminReview"
  },
  "clientSource": "String"
}
```

