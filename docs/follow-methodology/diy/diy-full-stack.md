# DIY Full-Stack

On this page, we wrote a meta guidelines pointing to various assets and instructions to rebuild the full-stack of the Social Cash Transfer Use Case or to develop and add own Use Cases or Building Blocks.

{% hint style="danger" %}
Section under construction until 15.01.2024
{% endhint %}

<table><thead><tr><th width="171.33333333333331">Title</th><th width="386">Scope</th><th>Note</th></tr></thead><tbody><tr><td><strong>DIY Full-Stack</strong></td><td><ul><li>Social Cash Transfer Use Case Frontend</li><li>Social Cash Transfer Use Case Backend</li><li>X-Road as BB Information Mediator</li><li>Building Block Software: MOSIP, Mifos Payment Hub, iGrant.io, OpenIMIS</li><li>Building Block Emulator: Registries</li><li>Infrastructure</li></ul></td><td></td></tr></tbody></table>

## Guidelines

{% hint style="warning" %}
DIY Full-Stack deployment will take time! Did you find errors or gaps in the guidelines? Drop us feedback following the menu item on the top.
{% endhint %}

### Infrastructure

1. Follow the [guide to deploy the infrastructure](https://github.com/GovStackWorkingGroup/sandbox-infra/blob/main/docs/1-main.md)

### Build Procedures

1. Decide for manual deployment or continues integration (e.g. CircleCI)

### Deploy Building Blocks

1. MOSIP as Identity Building Block
   1. [Installation Instructions](https://govstack-global.atlassian.net/wiki/spaces/GH/pages/340852774/Deployment+Guide)
   2. [Images and additional artifacts](https://github.com/tf-govstack)
2. Mifos Payment Hub as Payment Building Block
   1. [Installation Instructions](https://mifos.gitbook.io/docs/payment-hub-ee/overview/installation-instructions)
   2. Images and additional artifacts
   3. [Configuration Procedure](https://docs.google.com/document/d/12WxWmR21sGUn64pioSKFlMxFQkNpRpYfz\_4\_eugl2Rg/edit?usp=sharing)
3. iGrant.io as Consent Building Block
4. OpenIMIS as Digital Registries Building Block
5. Building Block [Emulator ](../../explore-stack/building-blocks/emulators.md)

### Deploy Information Mediator

1. Follow the guide to deploy X-Road as Information Mediator Building Block
2. Follow the guide to connect Building Blocks and Use Case Backend via X-Road Security Server

### Use Case Frontend and Backend

1. Deploy [Unconditional Social Cash Transfer (USCT) Backend](https://github.com/GovStackWorkingGroup/sandbox-usecase-usct-backend/blob/main/docs/main.md)
2. Deploy [Unconditional Social Cash Transfer (USCT) Frontend](https://github.com/GovStackWorkingGroup/sandbox-usecase-usct-frontend)

OR

Build your own Use Case [by following our example](../best-practice-example-design-of-the-sandbox-building-permit-use-case/)

## Struggling with setting up the prototype?

{% content-ref url="get-deployment-support.md" %}
[get-deployment-support.md](get-deployment-support.md)
{% endcontent-ref %}

