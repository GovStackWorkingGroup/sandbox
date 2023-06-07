# Guidelines for building block Sandbox deployment

> GovStack Sandbox aims to be an **isolated, safe environment simulating** a small governmental
> e-service system (reference implementation of the GovStack approach). The Sandbox is not intended to be a production
> environment, and it does not contain sensitive data. It is a demonstration environment to **learn** and a technical
> environment to **test and develop** digital government services.

## Two approaches for deployment:

1. The building block deployment is self-contained and deployed inside the Sandbox (preferred). 
2. The building block implementation provides a gateway component that is deployed inside the Sandbox. The gateway
provides s GovStack-compliant API and transparently accesses the externally deployed application (details out of
 scope of this document, defined case by case).

At the core, the Sandbox deployment environment for building blocks is a basic Kubernetes cluster. Building blocks deployed inside the Sandbox are not directly exposed to the public Internet.

## General guidelines

### OCI compliant container images
Building block applications should be provided as one or more OCI compliant container images (“Docker images”).

### Helm Chart
Container(s) of the application  should be packaged using a Helm (version 3) chart that defines the resources required by
the application. The chart should define a minimal, small scale deployment for exploration and development, covering only the essential
components and functionality.

* * For example, if the application uses a database, the deployment should define one.

### Basic Kubernetes concepts
The deployment should only depend on basic Kubernetes concepts and abstractions (e.g. deployments, pods, config maps,
secrets, services, persistent volume claims).

### Kubernetes Namespace
The application should be isolated into a Kubernetes namespace. The namespace name should be configurable during the
chart install time.

### Do not expect control of the cluster
An application can not expect control of the cluster, and should not depend on advanced features like custom Kubernetes
controllers.

### Not Expose any interfaces
The application should not expose any interfaces (e.g. ingresses should be opt-in or disabled).

### No external dependencies
The application should not, in general, require access to external resources in the Internet, but it can use other 
building blocks deployed in the same Sandbox.

### Configurable deployment
The deployment should include means for providing initial configuration for the application. For example, 
the application can provide additional configuration APIs, read configuration provided via a ConfigMap at deployment 
 time, or the configuration can be (partially) baked in to the container images. The exact mechanism is implementation 
 specific, but should be scriptable (not require manual steps or using a UI).

### Automatic deployment
The deployment should be fully automated so that the deployment can be triggered e.g. from a
CI/CD pipeline. Installing the chart with possible additional deployment-time configuration should start the application
in a known, working state.

### Tests
Preferably, the deployment should include basic tests that can be used to verify a successful deployment, and it
should be possible to integrate the tests to the pipeline.

## Examples
These examples are candidate building blocks and work in progress.

* [Information mediator BB](https://github.com/GovStackWorkingGroup/sandbox-bb-information-mediator)
* [Payment BB](https://github.com/GovStackWorkingGroup/sandbox-bb-payments)
* [Registration BB](https://github.com/GovStackWorkingGroup/sandbox-bb-registration)