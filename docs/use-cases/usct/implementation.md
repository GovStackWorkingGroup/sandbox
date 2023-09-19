# USCT demo implementation Demo Implementation (POC)
{% hint style="warning" %}
This section is under development.
{% endhint %}


## Frontend Application

{% hint style="warning" %}
This section is under development.
{% endhint %}

### Backend Application

{% hint style="warning" %}
This section is under development.
{% endhint %}

### Used Building Block Implementations

Building block implementations are applications that implement the functionality described in Govstack Specifications and are compliant with the defined API endpoints in Govstack Specifications.

Building Block Implementations that are used in current versions of UCST implementation are:

Building Block| Building Block Implementation | Documentation | Use case Version
--------------|-------------------------------|---------------|-----------------
[Payments](https://govstack.gitbook.io/bb-payments/)| [X-ROAD](https://github.com/GovStackWorkingGroup/sandbox-bb-information-mediator/tree/main/x-road)| [Documentation](https://github.com/GovStackWorkingGroup/sandbox-bb-information-mediator/blob/main/x-road/README.md) | 1.0.0

Building Block Implementations that will be used in next versions of UCST implementation are:

Building Block                                      | Building Block Implementation  | Documentation    | Use case Version
----------------------------------------------------|--------------------------------|------------------|-----------------
[Payments](https://govstack.gitbook.io/bb-payments/)| Mifos Payment HUB)             | TBD              | 1.X.X
[Identity](https://govstack.gitbook.io/bb-identity/)| Mosip                          | TBD              | 1.X.X

### Used Building Block Emulators

Building block emulators are simple application that “emulates“ the behaviour of specific building block (BB). The implementations are based on Govstack Specification. They are example implementation that mimics the actual behaviour of BB. They may not provide the complete functionality of specific BB, but should provide specified endpoints in the Govstack Specification.

Tech requirements:
* Java 17/Spring Boot 3.1 (latest stable versions)
* Gradle as a build tool
* Packaged as containers
* Minimal Helm chart for Kubernetes deployment

Additional requirements:
* Health check endpoints (org.springframework.boot:spring-boot-starter-actuator)
* Structured logging (net.logstash.logback:logstash-logback-encoder), to be able to output logs in JSON format for easier collecting.
* Swagger UI
* Open API spec JSON & YAML

Emulators should provide necessary API endpoints for Specific Application to accomplish specific use-case. In that case emulator should provide only the endpoints that are needed for specific use-case, and should evolve only when new use-case requires not yet implemented API endpoints.

Building Block emulators that are used in current version of UCST implementation are:

Building Block | Building Block Emulator | Documentation | Use case Version
---------------|-------------------------|---------------|-----------------
[Payments](https://govstack.gitbook.io/bb-payments/)| [Emulator](https://github.com/GovStackWorkingGroup/sandbox-bb-payments/tree/main/emulator) | [Documentation](https://github.com/GovStackWorkingGroup/sandbox-bb-payments/blob/main/emulator/docs/1-main.md) | 1.0.0
[Payments](https://govstack.gitbook.io/bb-payments/)| [Adapter to Emulator](https://github.com/GovStackWorkingGroup/sandbox-bb-payments/tree/main/adapter) | [Documentation](https://github.com/GovStackWorkingGroup/sandbox-bb-payments/blob/main/adapter/docs/1-main.md) | 1.0.0

Building Block emulators that will be used in next versions of UCST implementation are:

Building Block | Building Block Emulator | Documentation | Use case Version
---------------|-------------------------|---------------|-----------------
 [Digital Registries](https://govstack.gitbook.io/bb-digital-registries/) | [Emulator](https://github.com/GovStackWorkingGroup/sandbox-bb-digital-registries/tree/main/emulator) | [Documentation](https://github.com/GovStackWorkingGroup/sandbox-bb-digital-registries/blob/main/emulator/docs/main.md) | 1.X.X

