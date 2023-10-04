# Emulators

> [!IMPORTANT]
> Building block emulators are simple application that “emulates“ the behaviour of specific building block (BB). The implementations are based on Govstack Specification. They are example implementation that mimics the actual behaviour of BB. They may not provide the complete functionality of specific BB, but should provide specified endpoints in the Govstack Specification.
> Emulators should provide necessary API endpoints for Specific Application to accomplish specific use-case. In that case emulator should provide only the endpoints that are needed for specific use-case, and should evolve only when new use-case requires not yet implemented API endpoints.

> [!NOTE]
> In practical terms, an 'emulator' can be likened to a flight simulator employed to train pilots before the actual aircraft is constructed and tested. Similarly, in our context, a emulator is employed to support the development of use-cases before actual building block to be developed.
## Requirements

### Tech requirements:
* Java 17/Spring Boot 3.1 (latest stable versions)
* Gradle as a build tool
* Packaged as containers
* Minimal Helm chart for Kubernetes deployment

### Additional requirements:
* Health check endpoints (org.springframework.boot:spring-boot-starter-actuator)
* Structured logging (net.logstash.logback:logstash-logback-encoder), to be able to output logs in JSON format for easier collecting.
* Swagger UI
* Open API spec JSON & YAML

## Building Block emulator implementations:

| Building Block                                                           | Building Block Emulator                                                                              | Documentation                                                                                                          | SPEC Version |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------|
| [Payments](https://govstack.gitbook.io/bb-payments/)                     | [Emulator](https://github.com/GovStackWorkingGroup/sandbox-bb-payments/tree/main/emulator)           | [Documentation](https://github.com/GovStackWorkingGroup/sandbox-bb-payments/blob/main/emulator/docs/1-main.md)         | 1.0          |
| [Digital Registries](https://govstack.gitbook.io/bb-digital-registries/) | [Emulator](https://github.com/GovStackWorkingGroup/sandbox-bb-digital-registries/tree/main/emulator) | [Documentation](https://github.com/GovStackWorkingGroup/sandbox-bb-digital-registries/blob/main/emulator/docs/main.md) | 1.0          |

## Emulator Adaptor implementations:

> [!IMPORTANT]
>Adaptors are used to map existing APIs and functionality in a Digital Public Good into a format and scheme that is compatible with the GovStack API specifications.
>Adaptors may transform data formats (ie. XML to json), may transform URLs/protocols, or may be used to map GovStack APIs and data structures into sector-specific standards (ie. FHIR patient records).
>An adaptor (A) represents a candidate-specific solution to the delta between the API defined in the BB spec (GS) and the actual API (X) of candidate “X”. That’s A = GS - X .

> [!NOTE]
> In a practical sense, an 'adaptor' can be compared to a waiter who translates client orders into requests for the chef. Likewise, in our scenario, an adaptor is utilized to facilitate the transformation of requests for the building blocks.

| Building Block                                       | Building Block Adapter                                                                   | Building Block to adapt                                                                    | Documentation                                                                                                 | Spec Version |
|------------------------------------------------------|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|--------------|
| [Payments](https://govstack.gitbook.io/bb-payments/) | [Adapter](https://github.com/GovStackWorkingGroup/sandbox-bb-payments/tree/main/adapter) | [Emulator](https://github.com/GovStackWorkingGroup/sandbox-bb-payments/tree/main/emulator) | [Documentation](https://github.com/GovStackWorkingGroup/sandbox-bb-payments/blob/main/adapter/docs/1-main.md) | 1.0          |
