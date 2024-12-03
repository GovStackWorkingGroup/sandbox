---
description: >-
  The GovStack Sandbox is a demonstration environment for digital teams from
  governments and service providers to learn and test how the GovStack approach
  can be implemented.
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: false
  pagination:
    visible: false
---

# Enter the Sandbox

<table data-view="cards" data-full-width="false"><thead><tr><th></th><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Early Warning Tech Demo</strong><br></td><td>Demonstrating GovStack architecture and a-sync data exchange</td><td><a href=".gitbook/assets/USCT V2.png">USCT V2.png</a></td><td><a href="access-demos/early-warning-tech-demo/">early-warning-tech-demo</a></td></tr><tr><td><strong>Social Cash Transfer</strong> <br><strong>Tech Demo</strong></td><td>Demonstrating the GovStack architecture and all stack layers</td><td><a href=".gitbook/assets/USCT V2.png">USCT V2.png</a></td><td><a href="access-demos/usct-use-case.md">usct-use-case.md</a></td></tr><tr><td><strong>Construction Permit</strong><br><strong>UX Demo</strong></td><td>Demonstrating service design, UX/UI BB usage and mobile first approach</td><td><a href=".gitbook/assets/Technical partv2.png">Technical partv2.png</a></td><td><a href="access-demos/construction-permit-use-case.md">construction-permit-use-case.md</a></td></tr><tr><td><strong>Do It Yourself</strong></td><td>Protoype your own use case with different supporting assets</td><td><a href=".gitbook/assets/DIY v2.png">DIY v2.png</a></td><td><a href="follow-methodology/do-it-yourself-guide/">do-it-yourself-guide</a></td></tr><tr><td><strong>Technical Stack</strong></td><td>Learn about our implementations on all architecture layers</td><td><a href=".gitbook/assets/Technical part v2.png">Technical part v2.png</a></td><td><a href="explore-stack/architecture.md">architecture.md</a></td></tr><tr><td><strong>Design Methodology</strong></td><td>Learn about best practices on UX and Frontend design</td><td><a href=".gitbook/assets/Background blue web.png">Background blue web.png</a></td><td><a href="follow-methodology/best-practice-example-design-of-the-sandbox-building-permit-use-case/">best-practice-example-design-of-the-sandbox-building-permit-use-case</a></td></tr></tbody></table>

{% hint style="success" %}
**What you will find here**

* Live e-service demos to see the GovStack’s architecture and methodology in action
* Technical documentation of the e-service demos
* Do-It-Yourself packages to learn and test specific aspects of GovStack

GovStack Sandbox is a demonstration and learning tool designed to showcase and explore how digital government services can be built using modular, reusable building blocks.
{% endhint %}

{% hint style="danger" %}
**What you won't find here**

* Technical building block specifications of GovStack (find them on [GovSpecs](https://www.govstack.global/our-offerings/govspecs/))
* Ready-made software solutions you can integrate into your government infrastructure (find a list of possible solutions on [GovMarket](https://www.govstack.global/our-offerings/govmarket/))

GovStack Sandbox is not intended for building, deploying live systems. It is not a production-ready system.
{% endhint %}

{% hint style="info" %}
Building Block Software currently deployed in the environment (no recommendation, see long list of possible software applications on [GovMarket](https://www.govstack.global/software/)):

* X-Road (Information Mediator)
* Kafka (Information Mediator)
* MOSIP (Identity)
* iGrant.io/Redpill (Consent)
* Mifos Payment Hub (Payment)
* Baserow (Registry)
* OpenIMIS (Registry)
* Joget (Registration + Registry + Workflow)
* RapidPro (Messaging)
{% endhint %}

## Sandbox <mark style="background-color:blue;">Value Proposition</mark>

### <mark style="background-color:blue;">Learn</mark> about one possible implementation of the GovStack Specifications

In the Access Demo section, Explore Stack section and our [GitHub repositories](https://github.com/GovStackWorkingGroup?q=sandbox\&type=all\&language=\&sort=), you can dive step-by-step deeper into the technical implementation details.

* Access our demo implementations
  * [Early Warning Use Case](access-demos/early-warning-tech-demo/) - a UX and technology demo showcasing a-synchronous data exchange and usage of Messaging Building Block
  * [Social Cash Transfer Use Case](access-demos/usct-use-case.md) - a technology demo showcasing Building Block architecture
  * [Construction Permit Use Case](access-demos/construction-permit-use-case.md) - a UX demo showcasing the methodology from service design to frontend development
  * [High School Certificate Use Case](access-demos/high-school-certificate-methodology-demo.md) - a methodology demo showcasing the usage of service design templates
* Explore the [Sandbox architecture](explore-stack/architecture.md) and how the stack layers are build
* Read about the [Digital Public Infrastructure & Goods (DPI/DPG)](explore-stack/building-blocks/) we procured and customized from the open market
* Examine our [code repositories and developer documentation](./#sandbox-developer-documentation-and-code-repositories-github) containing: cloud infrastructure configurations; Helm charts; RPC layer for rapid prototyping; Building Block Emulator examples and many more.

### <mark style="background-color:blue;">Prototype</mark> with reusable assets to create your own use cases

Re-usability as one of GovStack's core principles, let us to develop all assets under Open Source licence and as much as possible as a generic implementation to be re-used for new use case prototypes.

* Follow our [service design best practice](follow-methodology/best-practice-example-design-of-the-sandbox-building-permit-use-case/) to implement according to the [GovStack Playbook](https://govstack.gitbook.io/implementation-playbook/)
* Use our ready-made [figma templates for user journeys and service blueprints](follow-methodology/best-practice-example-design-of-the-sandbox-building-permit-use-case/templates.md)
* [DIY-Package "Light"](follow-methodology/diy/usct-diy-version.md) of Social Cash Transfer Use Case to deploy a prototype comprising the Building Block architecture with lightweight [emulators](explore-stack/building-blocks/emulators.md) (enables you to e.g. access admin panels of X-Road, change data or API calls)
* [DIY-Instructions "Full Stack"](follow-methodology/diy/diy-full-stack.md) of Social Cash Transfer Use Case
* More assets in development!

### <mark style="background-color:blue;">Customize</mark> to your own needs local context

A customized version of the sandbox can take various forms and typically involves a software developer team. Possible customization projects could be: (a) providing mainly infrastructure and DevOps components to standardize deployment and configuration of Building Block software from your local GovTech companies or (b) recreating the full stack with different use cases and Building Block software.

[Contact us](https://www.govstack.global/about/contact/) to explore all the possibilities together.

{% hint style="info" %}
You might also enjoy our [GovStack Simulation](https://www.govstack.global/our-offerings/govspecs/simulation/) making the Building Block approach tangible **for less tech-savvy users**.
{% endhint %}

## <mark style="background-color:blue;">Table of Contents</mark>

### GovStack General

| [GovStack Initiative Website](https://www.govstack.global/) | [GovStack Specifications](https://govstack.gitbook.io/specification/) | [GovStack GitHub](https://github.com/GovStackWorkingGroup) |
| ----------------------------------------------------------- | --------------------------------------------------------------------- | ---------------------------------------------------------- |

### Sandbox High-Level Documentation (GitBook)

| <p><a href="access-demos/early-warning-tech-demo/">Early Warning Use Case Demo</a><br><a href="access-demos/usct-use-case.md">Social Cash Transfer Use Case Demo</a></p><p><a href="access-demos/construction-permit-use-case.md">Construction Permit Use Case Demo</a></p><p><a href="access-demos/high-school-certificate-methodology-demo.md">High School Certification Use Case Demo</a></p><p></p> | <p><a href="follow-methodology/do-it-yourself-guide/">Learning Paths</a></p><p><a href="follow-methodology/diy/">Do It Yourself</a><br><a href="follow-methodology/best-practice-example-design-of-the-sandbox-building-permit-use-case/">Service Design Practice</a></p> | <p><a href="explore-stack/architecture.md">Architecture</a></p><p><a href="explore-stack/use-case-frontend.md">Use Case Frontend</a></p><p><a href="explore-stack/use-case-backend.md">Use Case Backend</a></p><p><a href="explore-stack/building-blocks/">Building Blocks</a></p><p><a href="explore-stack/infrastructure.md">Infrastructure</a></p> |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

### Sandbox Developer Documentation and Code Repositories (GitHub)

| <p><a href="https://github.com/GovStackWorkingGroup/sandbox-infra">Infrastructure </a></p><p><a href="https://github.com/GovStackWorkingGroup/sandbox-app-rpc-backend">Generic RPC Backend</a><br><a href="https://github.com/GovStackWorkingGroup/sandbox-bb-emulator">Generic BB Emulator</a></p> | <p><a href="https://github.com/GovStackWorkingGroup/sandbox-usecase-usct-frontend">Social Cash Transfer (USCT) Use Case Frontend</a></p><p><a href="https://github.com/GovStackWorkingGroup/sandbox-usecase-usct-backend">Social Cash Transfer (USCT) Use Case Backend</a></p> | <p><a href="https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend">Construction Permit Use Case Frontend</a></p><p><a href="https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-backend">Construction Permit Use Case Backend</a></p> | [Early Warning Use Case Repositories](access-demos/early-warning-tech-demo/#how-are-the-stack-components-assembled) |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |

## Acknowledgement

Special thanks to all the contributors to the project:

[Gofore](https://gofore.com/en/) for implementing the concept of sandbox for Govstack and integrating BB. Especially:  Diego Martin; Vuk Damjanovic; Jarkko Hyöty; Bert Viikmäe; Kimmo Hedemäki; Heidi Kuum; Martha Vasquez; Oleksii Danyliuk; Priit Puru; Vladislav Todorov; Tsvetomir Krumov; Akseli Karvinen; Artun Gurkan; Jonas Bergmeier; Valentin Filyov; Vasil Kolev; Meelis Zujev; Harri Mansikamäki.

[Technoforte](https://www.technoforte.co.in/) for customizing and supplying MOSIP (Identity BB).

Mifos Consortium for customizing and supplying Mifos Payment Hub (Payment BB).

Nortal for customizing and supplying X-Road (Information Mediator BB).
