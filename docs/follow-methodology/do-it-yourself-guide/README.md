# Do It Yourself Guide

Guide your digital team through the suggested DIY path or pick your suitable steps to understand key design and architecture principles of GovStack. Accomplishing all or selected steps on this guide is a perfect practice for prototyping and implementing services based on the GovStack approach.

<figure><img src="../../.gitbook/assets/20240422_Infographic GovTest.png" alt="" width="375"><figcaption></figcaption></figure>

## Part 1: Service Design

**Participants:** Business Analysts, Domain Experts, UX Designers

**Objective:** Design a selected use case to a developer-ready stage and learn methodology along the way

**Deliverables:** User Journey(s), Service Blueprint, Wireframes

**Pre-Step:** Inform yourself about the suggest GovStack methodology

* [GovStack Playbook User Journey Description](https://govstack.gitbook.io/implementation-playbook/govstack-implementation-playbook/adopt-govstack/design-and-delivery/user-journeys)
* [GovStack UX/UI Guidelines](https://govstack.gitbook.io/specification/govstack-ui-ux-guidelines/2-description)
* GovStack Sandbox Example Service: Construction Permit
  * [Project Documentation](https://govstack.gitbook.io/sandbox/follow-methodology/best-practice-example-design-of-the-sandbox-building-permit-use-case)
  * [Use Case Frontend Demo](https://govstack.gitbook.io/sandbox/access-demos/construction-permit-use-case)

**Steps**

1. Draft an <mark style="background-color:blue;">**'As-Is' User Journey**</mark> to help identify touch points, inefficiencies, pain points, opportunities for improvement followed by a digitized <mark style="background-color:blue;">**'To-Be' user journey**</mark> that represents the desired state of the user experience after changes have been made
   * Select a use case with your team
   * Create As-Is and To-Be Use Journeys using the [User Journey Template](https://www.figma.com/file/w9oqWWuuxWtab5EPJIVhhA/Journey-Template?type=whiteboard\&node-id=0-1\&t=8wa9qG3v6V37ga9W-0) (click on the arrow next to the title to duplicate the template)
   * For an introduction to the template, watch our explanatory [User Journey video](https://www.youtube.com/watch?v=sKnTfcUm2z4)
   * As a workshop method, you may use the [GovStack Design Sprint](https://govstack.gitbook.io/sandbox/follow-methodology/govstack-design-sprint) proposal
2. Develop a <mark style="background-color:blue;">**Service Blueprint**</mark> which helps organizations see the big picture of how a service is implemented and used. It pinpoints required Building Blocks, dependencies between user journeys and government entities in the same visualization.&#x20;
   * Create a Service Blueprint using the [Service Blueprint Template](https://www.figma.com/file/SjEyL4ClDkOiLMsMQwkXig/Service-Blueprint-Template?type=whiteboard\&node-id=0-1\&t=JXvpoBn7bDgDQP05-0)
   * For an introduction to the template, watch our explanatory [Service Blueprint video](https://www.youtube.com/watch?v=ALUlf7fJY9I)
3. Create <mark style="background-color:blue;">**Wireframes**</mark> to outline the user interface and interaction flow, serving as a base for the visual and functional aspects of the digitized solution.
   * Create wireframes using the [GovStack Wireframe Kit](https://govstack.gitbook.io/sandbox/follow-methodology/diy/diy-wireframes)

Success! The service design team is ready to hand over the service to the developers.

## Part 2: Software Development

**Target group:** IT Architects, Software Engineers and Backend Developers

**Objective:** Build a testing environment and learn how GovStack architecture can be technically implemented in practice

**Deliverables:** Deployed of Sandbox in any form

**Pre-Step:** Inform yourself about the technical theory and practice of the GovStack approach

* Get familiar with the Building Block architecture using [GovStack architecture](https://govstack.gitbook.io/specification/architecture-and-nonfunctional-requirements) specifications and[ Building Block specifications](https://govstack.gitbook.io/specification/building-blocks/about-building-blocks)
* Compare specification and actual implementation of concepts like “Building Blocks”, “Information Mediator Security Server”, “Emulators”, “Adapters”, … using [GovStack Sandbox USCT Technical Demo](https://govstack.gitbook.io/specification/building-blocks/about-building-blocks)
  * [High-level explanation of the software stack](https://govstack.gitbook.io/sandbox/explore-stack/architecture)
  * [Developer Documentation of the Use Case Demo](https://github.com/GovStackWorkingGroup/sandbox-usecase-usct-backend/blob/main/docs/main.md)
  * [GitHub Code Repositories](https://github.com/GovStackWorkingGroup?q=sandbox\&type=all\&language=\&sort=)

**Steps** (All steps can be conducted chronologically or on an individual basis and need)

1. Service Design (see above)
2. "
3. "
4. Develop a <mark style="background-color:blue;">**Frontend**</mark>. It outlines the user interface and interaction flow, displaying real visual and functional aspects of the digitized solution. Create your own Frontend according to your use case and your needs.
   * If you end or pause with this prototype, you might add Functionality with our [generic RPC backend](../diy/diy-dynamic-frontend/)
5. Download <mark style="background-color:blue;">**GovStack’s Sandbox**</mark> environment (Minikube container with Use Case Frontend + X-Road + BB Emulator) and deploy and configure X-Road (a possible software for Information Mediator Building Block). Learn how Building Blocks interact via X-Road with the Frontend based on GovStack’s use case “Social Cash Transfer”.
   * [Sandbox Minikube Explanatory Videos](https://govstack.gitbook.io/sandbox/follow-methodology/diy/usct-diy-version)
   * [Sandbox Minikube Github Docs](https://github.com/GovStackWorkingGroup/sandbox-usecase-usct-backend/blob/main/docs/diy.md)
6. Build <mark style="background-color:blue;">**Your Emulated Sandbox**</mark> by recreating GovStack’s Sandbox and extend it with your Frontend and Building Block Emulators needed according to your Service Blueprint.
   * Rebuild [infrastructure layer](https://github.com/GovStackWorkingGroup/sandbox-infra)
   * Deploy [Information Mediator "X-Road"](../diy/diy-full-stack.md#deploy-information-mediator)
   * Deploy your Frontend from step 1
   * Build [Building Block Emulators](../../explore-stack/building-blocks/emulators.md) for each BB required according to the Service Blueprint
   * Integrate all components; you might find guidance based on our [Social Cash Transfer Demo Github Repositories](../../access-demos/usct-use-case.md#how-are-the-stack-components-assembled)
7.  Assemble <mark style="background-color:blue;">**Your Full-Stack Sandbox**</mark> using open source software and assets provided by GovStack, your own Frontend and any Building Block Software of your choice.

    (Extensive knowledge required)

    * Follow step 3
    * Exchange Building Block Emulators with actual Software solutions compliant to the GovStack Specifications
    * Optionally, follow [instructions to deploy Open Source Software for Identity, Payment and Consent Building Block](../diy/diy-full-stack.md)

Success! The developer team is ready to scale the testing environment with more citizen services or to bring that one prototype closer to production use.
