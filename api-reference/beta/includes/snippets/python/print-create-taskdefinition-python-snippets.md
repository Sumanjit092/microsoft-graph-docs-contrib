---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.print_task_definition import PrintTaskDefinition
from msgraph_beta.generated.models.app_identity import AppIdentity

graph_client = GraphServiceClient(credentials, scopes)

request_body = PrintTaskDefinition(
	display_name = "Test TaskDefinitionName",
	created_by = AppIdentity(
		display_name = "Requesting App Display Name",
	),
)

result = await graph_client.print.task_definitions.post(request_body)


```