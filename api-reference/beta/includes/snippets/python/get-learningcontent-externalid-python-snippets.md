---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.employee_experience.learning_providers.by_learning_provider_id('learningProvider-id').learning_contents_with_external_id("{externalId}").get()


```