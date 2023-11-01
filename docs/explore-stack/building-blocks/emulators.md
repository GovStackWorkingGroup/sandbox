# Emulators

Building block emulators are simple application that “emulates“ the behaviour of specific building block (BB). The implementations are based on Govstack Specification. They are example implementation that mimics the actual behaviour of BB. They may not provide the complete functionality of specific BB, but should provide specified endpoints in the Govstack Specification. Emulators should provide necessary API endpoints for Specific Application to accomplish specific use-case. In that case emulator should provide only the endpoints that are needed for specific use-case, and should evolve only when new use-case requires not yet implemented API endpoints.

{% hint style="info" %}
In practical terms, an 'emulator' can be likened to a flight simulator employed to train pilots before the actual aircraft is constructed and tested. Similarly, in our context, a emulator is employed to support the development of use-cases before actual building block to be developed.
{% endhint %}

## What do we use to <mark style="background-color:blue;">build</mark> it?

<table><thead><tr><th width="225">Name</th><th>Purpose</th></tr></thead><tbody><tr><td>Java 17/Spring Boot 3.1</td><td>Application framework</td></tr><tr><td>Gradle</td><td>Build tool</td></tr><tr><td>Helm chart</td><td>Kubernetes deployment</td></tr></tbody></table>

## Where do we <mark style="background-color:blue;">demo</mark> it?

### Building Block emulator implementations:

| Building Block                                                           | Building Block Emulator                                                                              | Documentation                                                                                                          | SPEC Version |
| ------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------ |
| [Payments](https://govstack.gitbook.io/bb-payments/)                     | [Emulator](https://github.com/GovStackWorkingGroup/sandbox-bb-payments/tree/main/emulator)           | [Documentation](https://github.com/GovStackWorkingGroup/sandbox-bb-payments/blob/main/emulator/docs/1-main.md)         | 1.0          |
| [Digital Registries](https://govstack.gitbook.io/bb-digital-registries/) | [Emulator](https://github.com/GovStackWorkingGroup/sandbox-bb-digital-registries/tree/main/emulator) | [Documentation](https://github.com/GovStackWorkingGroup/sandbox-bb-digital-registries/blob/main/emulator/docs/main.md) | 1.0          |

### Emulator Adaptor implementations:

Adaptors are used to map existing APIs and functionality in a Digital Public Good into a format and scheme that is compatible with the GovStack API specifications. Adaptors may transform data formats (ie. XML to json), may transform URLs/protocols, or may be used to map GovStack APIs and data structures into sector-specific standards (ie. FHIR patient records). An adaptor (A) represents a candidate-specific solution to the delta between the API defined in the BB spec (GS) and the actual API (X) of candidate “X”. That’s A = GS - X .

{% hint style="info" %}
In a practical sense, an 'adaptor' can be compared to a waiter who translates client orders into requests for the chef. Likewise, in our scenario, an adaptor is utilized to facilitate the transformation of requests for the building blocks.
{% endhint %}

For comprehensive details on Adaptors, please refer to the official GovStack [specification](https://govstack.gitbook.io/specification/architecture-and-nonfunctional-requirements/6-onboarding#6.1-adapters).

| Building Block                                       | Building Block Adaptor                                                                   | Building Block to adapt                                                                    | Documentation                                                                                                 | Spec Version |
| ---------------------------------------------------- | ---------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------- | ------------ |
| [Payments](https://govstack.gitbook.io/bb-payments/) | [Adaptor](https://github.com/GovStackWorkingGroup/sandbox-bb-payments/tree/main/adapter) | [Emulator](https://github.com/GovStackWorkingGroup/sandbox-bb-payments/tree/main/emulator) | [Documentation](https://github.com/GovStackWorkingGroup/sandbox-bb-payments/blob/main/adapter/docs/1-main.md) | 1.0          |

## Which <mark style="background-color:blue;">conceptual decisions</mark> do we follow?

* Health check endpoints (org.springframework.boot:spring-boot-starter-actuator)
* Structured logging (net.logstash.logback:logstash-logback-encoder), to be able to output logs in JSON format for easier collecting.
* Swagger UI
* Open API spec JSON & YAML
