---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.shares.by_shared_drive_item_id('sharedDriveItem-id').drive_item.get()


```