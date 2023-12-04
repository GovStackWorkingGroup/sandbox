# DIY dynamic frontend

This prototype can be used to only test and demo a functional frontend or do decouple frontend and backend development until it can be merged at a later point in time.

{% hint style="info" %}
Dynamic frontend implemented via RPC Layer concept that is based on the Facade Pattern. In short, we are using it as a configurable API layer. It allows us granular control over our API call method endpoints from one location, which is good for demonstrating connectivity between different interchangeable Building Blocks. In addition, the RPC layer can also be configured for different providers, such as MockProvider, APIProvider, LocalStorageProvider, etc.
{% endhint %}

## Dynamic frontend example implementation

The Front End Demo for Construction Permit Use Case illustrates the deployment of an automated service designed to streamline the entire process of approving construction permits. This comprehensive digital solution addresses challenges associated with conventional "over the counter" and paper-based permit management. Its primary objectives are to enhance transparency, accountability, and efficiency in overseeing construction practices to ensure they are safe and compliant with regulations.

Property owners, lead architects, engineers, or principal contractors can initiate the construction permit application process by providing the required information and documents online. Once the application is submitted, the applicant can monitor the approval progress and take additional actions that may arise during the process. These actions include:

- Uploading any additional documents required
- Scheduling inspections

Applicants receive notifications about changes in their application status, such as when a specific action is needed, when an inspection date is approaching, or when their application has been either approved or rejected. This real-time communication system enhances the overall experience and engagement of citizens throughout the construction permit approval journey.

### Construction Permit use case
The Construction Permit can switch between three providers:

| Provider         | Datasource                                                                                     | Resource                                                            |
| ---------------- | ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| Mock Provider    | Local in-app preset values for required data| [Mock Provider](https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend/blob/main/src/rpc/MockProvider.ts)    |                                                                     |
| API Provider     | [RPC Backend](#dynamic-frontend-storage-application-implementation) - Storage Application      | [API Provider](https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend/blob/main/src/rpc/APIProvider.ts)                         |
| Storage Provider | Browser's local storage / Data from Mock Provider if no data is available in the local storage | [Storage Provider](https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend/blob/main/src/rpc/StorageProvider/StorageProvider.ts) |

These providers extend the [Base Provider](https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend/blob/main/src/rpc/BaseProvider.ts) which acts as an interface for needed methods and api calls.

All three providers contain the business login in the front end and use the provider as data storage.

### Construction Permit use case guidelines

| Case        | Description | Resource |
| ----------- | ----------- | -------- |
| Run locally | Run application locally. Run like a react app | [GovStack GIT Repo](https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend/tree/main/docs/main.md)|
Docker        | Run application in Docker | [Docker](https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend/tree/main/docs/docker.md) |
Kubernetes    | Run application in k8s cluster using [HELM Chart](https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend/tree/main/docs/helm.md) | [Kubernetes](https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend/tree/main/docs/kubernetes.md)


Environment variables needed are described in [Configuration](https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend/tree/main/docs/configuration.md)

## Dynamic frontend storage application implementation

TODO: @Vladislav

### RPC backend storage application

TODO: @Vladislav

### RPC backend storage application guidelines

TODO: @Vladislav