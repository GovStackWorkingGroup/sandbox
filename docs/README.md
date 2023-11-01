---
description: Test and Learn the GovStack Approach using our Sandbox
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

The GovStack Sandbox is a demonstration environment for **digital teams from governments and service providers** to **learn** and **test** how to technically implement the GovStack approach.

<table data-view="cards" data-full-width="false"><thead><tr><th></th><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Access </strong><em><strong>Unconditional Social Cash Transfer (USCT)</strong></em><strong> Use Case Demo</strong></td><td>Demonstrating the GovStack architecture and all stack layers</td><td><a href=".gitbook/assets/USCT V2.png">USCT V2.png</a></td><td><a href="access-demos/usct-use-case.md">usct-use-case.md</a></td></tr><tr><td><strong>Access </strong><em><strong>Construction Permit</strong></em><strong> Use Case Demo</strong></td><td>Demonstrating service design, UX/UI BB usage and mobile first approach</td><td><a href=".gitbook/assets/Technical partv2.png">Technical partv2.png</a></td><td><a href="access-demos/construction-permit-use-case.md">construction-permit-use-case.md</a></td></tr><tr><td><strong>Do It Yourself</strong></td><td>Get reusable assets and example implementations on different ways of prototyping</td><td><a href=".gitbook/assets/DIY v2.png">DIY v2.png</a></td><td><a href="access-demos/diy/">diy</a></td></tr><tr><td><strong>Explore Technical Stack</strong></td><td>Learn about our implementations on all architecture layers</td><td><a href=".gitbook/assets/Technical part v2.png">Technical part v2.png</a></td><td><a href="explore-stack/architecture.md">architecture.md</a></td></tr><tr><td><strong>Follow Design Methodology</strong></td><td>Learn about best practices on UX and Frontend design</td><td><a href=".gitbook/assets/Background blue web.png">Background blue web.png</a></td><td><a href="follow-methodology/best-practice-example-design-of-the-sandbox-building-permit-use-case/">best-practice-example-design-of-the-sandbox-building-permit-use-case</a></td></tr></tbody></table>

{% hint style="info" %}
You might also enjoy our [GovStack Simulation](https://www.govstack.global/our-offerings/govspecs/simulation/) making the Building Block approach tangible **for less tech-savvy users**.
{% endhint %}

## What <mark style="background-color:blue;">value</mark> does the sandbox offer?

### Learn

The design of the GovStack sandbox encapsulates the business logic and data necessary to **represent multiple GovStack capabilities** such as APIs, Building Blocks, use cases and transaction flows. This helps developers and digital government agencies to achieve a more holistic view of the GovStack approach.

[Access the various demos](access-demos/usct-use-case.md) and [explore the software stack](explore-stack/architecture.md#what-do-we-use-to-build-it) behind these demos. Additionally, you can learn from our development experience at [follow methodology](follow-methodology/best-practice-example-design-of-the-sandbox-building-permit-use-case/).

### Test

The fully operational environment offers a comprehensive API that public and private agencies can use to **mimic the characteristics exhibited by the GovStack Specifications**. Therefore, it offers an environment on a real-time basis to help **simulate responses** from all the systems an application interfaces with. This especially enables digital government players to **experiment with innovative GovTech products or services** within a well-defined space and duration.&#x20;

[Deploy a replication](access-demos/diy/usct-diy-version.md) of the GovStack Sandbox and experiment with the software architecture.

### Reuse

In addition to the demo and test purpose, the Sandbox offers a [publicly available kit of reusable tools](access-demos/diy/), including:

* Cloud infrastructure configurations
* Container images
* CI/CD pipeline configurations
* Helm charts for Building Blocks
* RPC layer for rapid prototyping
* Building Block Emulator examples

## What <mark style="background-color:blue;">value</mark> does the sandbox <mark style="background-color:blue;">not</mark> offer?

* The Sandbox is _not_ an off-the-self testing environment for your countries e-Government stack. To resemble your IT systems and therefore be of practical testing use for your existing IT context, you would need to customize the Sandbox.

## Where can I <mark style="background-color:blue;">find ...</mark> ?

### GovStack General

| [GovStack Initiative Website](https://www.govstack.global/) | [GovStack Specifications](https://govstack.gitbook.io/specification/) | [GovStack GitHub](https://github.com/GovStackWorkingGroup) |
| ----------------------------------------------------------- | --------------------------------------------------------------------- | ---------------------------------------------------------- |

### Sandbox High-Level Documentation (GitBook)

| <p><a href="access-demos/usct-use-case.md">USCT Use Case Demo</a></p><p><a href="access-demos/construction-permit-use-case.md">Construction Permit Use Case</a></p><p><a href="access-demos/diy/">Do It Yourself</a></p> | <p><a href="explore-stack/architecture.md">Architecture</a></p><p><a href="explore-stack/use-case-frontend.md">Use Case Frontend</a></p><p><a href="explore-stack/use-case-backend.md">Use Case Backend</a></p><p><a href="explore-stack/building-blocks/">Building Blocks</a></p><p><a href="explore-stack/devops.md">DevOps</a></p><p><a href="explore-stack/infrastructure.md">Infrastructure</a></p> | <p><a href="follow-methodology/best-practice-example-design-of-the-sandbox-building-permit-use-case/">Service Design</a></p><p><a href="follow-methodology/frontend-development.md">Frontend Development</a></p><p><a href="faq.md">FAQ</a></p><p><a href="version-history.md">Version History</a></p> |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |

### Sandbox Developer Documentation and Code Repositories (GitHub)

| <p><a href="https://github.com/GovStackWorkingGroup/sandbox-infra">Infrastructure </a></p><p><a href="https://github.com/GovStackWorkingGroup/sandbox-app-rpc-backend">Generic RPC Backend</a><br><a href="https://github.com/GovStackWorkingGroup/sandbox-bb-emulator">Generic BB Emulator</a></p> | <p><a href="https://github.com/GovStackWorkingGroup/sandbox-usecase-usct-frontend">USCT Use Case Frontend</a></p><p><a href="https://github.com/GovStackWorkingGroup/sandbox-usecase-usct-backend">USCT Use Case Backend</a></p> | <p><a href="https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend">Construction Permit Use Case Frontend</a></p><p><a href="https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-backend">Construction Permit Use Case Backend</a></p> |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

## Acknowledgement

Special thanks to all the contributors to the project:

[Gofore](https://gofore.com/en/) for implementing the concept of sandbox for Govstack and integrating BB. Especially: Jarkko Hyöty; Bert Viikmäe; Kimmo Hedemäki; Heidi Kuum; Martha Vasquez; Oleksii Danyliuk; Priit Puru; Vladislav Todorov; Tsvetomir Krumov; Akseli Karvinen; Artun Gurkan; Jonas Bergmeier; Valentin Filyov; Vasil Kolev; Meelis Zujev; Harri Mansikamäki.

[Technoforte](https://www.technoforte.co.in/) for customizing and supplying MOSIP (Identity BB).

Mifos Consortium (...) for customizing and supplying Mifos Payment Hub (Payment BB).

Nortal for customizing and supplying X-Road (Information Mediator BB).
