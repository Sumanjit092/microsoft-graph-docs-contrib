---
description: "Automatically generated file. DO NOT MODIFY"
---

```bash


mgc-beta security alerts update-alerts post --body '{\
  "value": [\
    {\
      "assignedTo": "String",\
      "closedDateTime": "String (timestamp)",\
      "comments": ["String"],\
      "feedback": {"@odata.type": "microsoft.graph.alertFeedback"},\
      "id": "String (identifier)",\
      "status": {"@odata.type": "microsoft.graph.alertStatus"},\
      "tags": ["String"],\
      "vendorInformation":\
        {\
          "provider": "String",\
          "vendor": "String"\
        }\
    }\
  ]\
}\
'

```