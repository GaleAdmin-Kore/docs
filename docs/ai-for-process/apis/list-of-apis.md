# List of AI for Process APIs

The APIs list provides a consolidated reference of all APIs available in AI for Process. These APIs enable developers to programmatically perform key operations across the platform, including uploading files, tracking process statuses, and managing tools and models through actions such as import, export, deployment, and undeployment. All API requests require authentication using an API key, which the account owner or admin can generate from the Settings console.

## File Management API

| Use Cases   | API     |
|--------|----------|
| Upload a small or large public file in the [supported formats](apis-list/upload-file-api.md){:target="_blank"}. | [File Upload API](apis-list/upload-file-api.md){:target="_blank"} |

## View Process Status API

| Use Cases   | API     |
|--------|----------|
| Check the status of an ongoing or completed job related to tools or models. | [Get Dock Status API](apis-list/get-dock-status.md){:target="_blank"} |

## Manage Tools APIs

| Use Cases   | APIs    |
|--------|----------|
| Import a new tool.     |  [Import a New Tool API](apis-list/import-a-new-tool.md){:target="_blank"} |
| Import new configurations, datasets, or updates into a tool.      |   [Import to an Existing Tool API](apis-list/import-to-an-existing-tool.md){:target="_blank"} |
| Export a tool's configuration and associated data, including its flow, for backup, sharing, or reuse.      | [Export a Tool API](apis-list/export-a-tool.md){:target="_blank"} |
| Deploy a specific tool into an environment. | [Deploy a Tool API](apis-list/deploy-a-tool.md){:target="_blank"} |
| Undeploy a specific tool from an environment. | [Undeploy a Tool API](apis-list/undeploy-a-tool.md){:target="_blank"} |

## Manage Models APIs

| Use Cases  | APIs     |
|--------|----------|
|  Import a model in chunks.     |    [Import a Model API](apis-list/import-a-model.md){:target="_blank"}      |
|  Export a trained AI model.     |   [Export a Model API](apis-list/export-a-model.md){:target="_blank"}       |
| Deploy a model into the environment in the Ready to Deploy state and configure its parameters. You must perform the initial deployment manually in the Platform account. Consecutive deployments must happen via the public API.      | [Deploy a Model API](apis-list/deploy-a-model.md){:target="_blank"}         |
| Undeploy a model from the environment.      |   [Undeploy a Model API](apis-list/undeploy-a-model.md){:target="_blank"} |
| Manage external model connections.      |   [External Model Connection APIs](apis-list/connections-api.md){:target="_blank"} |
