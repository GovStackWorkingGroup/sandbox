# Building Blocks

Building blocks (BBs) are software modules that can be deployed and combined in a standardized manner. Each building block is capable of working independently, but they can be combined to do much more. Read the [full definition in the GovStack Specifications](https://govstack.gitbook.io/specification/architecture-and-nonfunctional-requirements/introduction#2.3-building-blocks).

## What do we use to <mark style="color:blue;">build</mark> it?

The Building Block Software are build based on various different software stacks. Please visit the respective documentations for more insights.&#x20;

| BB Software                                  | GovStack Specification Compliance                                                                |
| -------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| [MOSIP](https://docs.mosip.io/)              | [Identity Specification 1.0](https://govstack.gitbook.io/bb-identity/)                           |
| [X-Road](https://docs.x-road.global/)        | [Information Mediator Specification 1.0](https://govstack.gitbook.io/bb-information-mediation/)  |
| [Mifos Payment Hub](https://docs.mifos.org/) | [Payment Specification 2.0](https://govstack.gitbook.io/bb-payments/)                            |
| Payment Emulator                             | [Payment Specification 1.0](https://govstack.gitbook.io/bb-payments/)                            |
| Payment Adapter                              | [Payment Specification 1.0 Service APIs](https://govstack.gitbook.io/bb-payments/9-service-apis) |

For our Building Block Emulators, visit our [sub page on emulators](emulators.md).

## Where do we <mark style="color:blue;">demo</mark> it?&#x20;

### Building Block Software in Use

| GitHub Repository                                                                                                 | Used in...                                                                                                      |
| ----------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| MOSIP                                                                                                             | [USCT](https://github.com/GovStackWorkingGroup/sandbox-usecase-usct-backend/blob/main/docs/main.md)             |
| [X-Road](https://github.com/GovStackWorkingGroup/sandbox-bb-information-mediator)                                 | <p><a href="../../access-demos/usct-use-case.md">USCT</a><br><a href="../../access-demos/diy/">USCT DIY</a></p> |
| Mifos Payment Hub                                                                                                 | [USCT](../../access-demos/usct-use-case.md)                                                                     |
| [Payment Emulator](https://github.com/GovStackWorkingGroup/sandbox-bb-payments/blob/main/emulator/docs/1-main.md) | [USCT DIY](../../access-demos/diy/)                                                                             |
| [Payment Adapter](https://github.com/GovStackWorkingGroup/sandbox-bb-payments/blob/main/adapter/docs/1-main.md)   | [USCT DIY](../../access-demos/diy/)                                                                             |

### Building Block Software in Progress

| BB Implementation      | BB Specification Compliance | Status         |
| ---------------------- | --------------------------- | -------------- |
| iGrant.io              | Consent Specification 1.0   | In Development |
| OpenIMIS               | Registry Specification 1.0  | In Development |
| Platform of Registries | Registry Specification 1.0  | Planned        |

## Which <mark style="color:blue;">decisions</mark> do we follow?

The Building Block Implementations listed here have been openly procured by GovStack Initiative based on the GovStack Specifications. The providers of these BB implementations have been assigned to adapt/extend their offered software solutions to fully meet the GovStack Specifications for the respective Building Block. You can read more on our [efforts to contribute these additional features to the software's upstream](../../follow-methodology/our-dpi-dpg-contributions.md).

## Further documentation
