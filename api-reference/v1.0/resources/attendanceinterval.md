---
title: "attendanceInterval resource type"
description: "Contains information associated with an attendance interval in an attendanceRecord."
author: "mkhribech"
ms.localizationpriority: medium
ms.prod: "cloud-communications"
doc_type: resourcePageType
---

# attendanceInterval resource type

Namespace: microsoft.graph

Contains information associated with an attendance interval in an [attendanceRecord](attendancerecord.md).

## Properties

| Property            | Type    | Description|
|:--------------------|:--------|:-----------|
| durationInSeconds | Int32 | Duration of the meeting interval in seconds; that is, the difference between **joinDateTime** and **leaveDateTime**. |
| joinDateTime | DateTime | The time the attendee joined in UTC. |
| leaveDateTime | DateTime | The time the attendee left in UTC. |

> [!TIP]
> When data is lacking, the value of **joinDateTime** or **leaveDateTime** will be set to `null`, and the value of **durationInSeconds** will be set to `0` in the response body of the [Get meetingAttendanceReport](/graph/api/meetingattendancereport-get?view=graph-rest-v1.0&preserve-view=true) method.

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attendanceInterval"
}-->

```json
{
    "durationInSeconds": "Int32",
    "joinDateTime": "String (timestamp)",
    "leaveDateTime": "String (timestamp)"
}
```
