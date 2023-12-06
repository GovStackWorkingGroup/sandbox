# DIY dynamic frontend

This prototype can be used to only test and demo a functional frontend or do decouple frontend and backend development until it can be merged at a later point in time.

{% hint style="info" %}
Dynamic frontend implemented via RPC Layer concept that is based on the Facade Pattern. In short, we are using it as a configurable API layer. It allows us granular control over our API call method endpoints from one location, which is good for demonstrating connectivity between different interchangeable Construction Blocks. In addition, the RPC layer can also be configured for different providers, such as MockProvider, APIProvider, LocalStorageProvider, etc.
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
Kubernetes    | Run application in k8s cluster using [HELM Chart](https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend/tree/main/helm) | [Kubernetes](https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend/tree/main/docs/kubernetes.md)


Environment variables needed are described in [Configuration](https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend/tree/main/docs/configuration.md)

## Dynamic frontend storage application implementation

For efficient data storage supporting the seamless exchange of information with the RPC layer, the application 'rpc-backend' serves as an ideal backend solution. It facilitates the storage, retrieval, and utilization of data crucial for the RPC layer's operations used when creating Dynamic Frontend Application covering specific use-case.
### RPC backend storage application

{% hint style="info" %}The RPC Backend represents an advanced backend storage application tailored to securely manage user and tenant-specific key-value pairs. It offers a robust framework for storing and organizing data.{% endhint %}

For example in Construction permit use case:

| Item   | Value             | Default                                            |
|--------|-------------------|----------------------------------------------------|
| tenant | "building-permit" | any string                                         |
| user   | "user1"           | One of 10 default users or any new registered user |


Actual implementation can be found in the following [GovStack Git Repo](https://github.com/GovStackWorkingGroup/sandbox-app-rpc-backend)

Documentation can be found in [GovStack Git Repo](https://github.com/GovStackWorkingGroup/sandbox-app-rpc-backend/blob/main/docs/main.md)

### RPC backend storage application guidelines

There are multiple ways to run and use the rpc-backend storage app. The different ways and respective resources can be found in the table below:

| Case       | Description                                                                                                                       | Resource                                                                                                                                                                                                                                             |
|------------|-----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Local Run  | Run application locally, useful for development purposes. Should be run as Spring Boot app.                                       | [GovStack Git Repo](https://github.com/GovStackWorkingGroup/sandbox-app-rpc-backend)                                                                                                                                                                 |
| Docker     | Run application as docker container                                                                                               | [Instructions Docker](https://github.com/GovStackWorkingGroup/sandbox-app-rpc-backend/blob/main/docs/docker.md)                                                                                                                                      |
| Kubernetes | Run application in k8s cluster using [Helm Chart](https://github.com/GovStackWorkingGroup/sandbox-app-rpc-backend/tree/main/helm) | [Instructions Helm](https://github.com/GovStackWorkingGroup/sandbox-app-rpc-backend/blob/main/docs/helm-install.md) & [Instructions Kubernetes](https://github.com/GovStackWorkingGroup/sandbox-app-rpc-backend/blob/main/docs/kubernetes-access.md) |

All environment variable definitions can be found in [GovStack Git Repo](https://github.com/GovStackWorkingGroup/sandbox-app-rpc-backend/blob/main/docs/env-vars.md)

{% hint style="info" %}All available endpoints can be found in [Main Documentation](https://github.com/GovStackWorkingGroup/sandbox-app-rpc-backend/blob/main/docs/main.md) after accessing swagger UI. Usage of endpoints is described in [API Usage](https://github.com/GovStackWorkingGroup/sandbox-app-rpc-backend/blob/main/docs/api.md).
{% endhint %}
