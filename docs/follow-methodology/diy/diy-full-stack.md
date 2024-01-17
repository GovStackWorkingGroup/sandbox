# DIY Full-Stack

On this page, we wrote a meta guidelines pointing to various assets and instructions to rebuild the full-stack of the Social Cash Transfer Use Case or to develop and add own Use Cases or Building Blocks.

<table><thead><tr><th width="171.33333333333331">Title</th><th width="386">Scope</th><th>Note</th></tr></thead><tbody><tr><td><strong>DIY Full-Stack</strong></td><td><ul><li>Social Cash Transfer Use Case Frontend</li><li>Social Cash Transfer Use Case Backend</li><li>X-Road as BB Information Mediator</li><li>Building Block Software: MOSIP, Mifos Payment Hub, iGrant.io, OpenIMIS</li><li>Building Block Emulator: Registries</li><li>Infrastructure</li></ul></td><td></td></tr></tbody></table>

## Guidelines

{% hint style="warning" %}
DIY Full-Stack deployment will take time! Did you find errors or gaps in the guidelines? Drop us feedback following the menu item on the top.
{% endhint %}

### Build Infrastructure

1. Follow the [guide to deploy the infrastructure](https://github.com/GovStackWorkingGroup/sandbox-infra/blob/main/docs/1-main.md)
2. Decide for manual deployment or use [continues integration](../../explore-stack/devops.md) (e.g. CircleCI) tools

### Deploy Information Mediator

1. X-Road as Information Mediator Building Block
   1. [Deployment and Configuration Instructions](https://github.com/nortal/GovStack-IM-BB-SandBox-Deployment)
   2. Code and artifact repositories
      1. [X-Road](https://iii.https/github.com/nortal/GovStack-IM-BB-X-Road)
      2. [X-Road Metrics](https://iv.https/github.com/nortal/GovStack-IM-BB-X-Road-Metrics)
      3. [PubSub Component](https://i.https/github.com/nortal/GovStack-IM-BB-PubSub-Component)
2. Connect Building Blocks and Use Case Backend of next chapter via X-Road Security Server
   1. [Deployment and Configuration Instructions](https://docs.x-road.global/Manuals/ug-ss\_x-road\_6\_security\_server\_user\_guide.html#table-of-contents)

### Deploy Building Blocks

1. MOSIP as Identity Building Block
   1. [Deployment and Configuration Instructions](https://govstack-global.atlassian.net/wiki/spaces/GH/pages/387055625/Updated+Deployment+Guide)
   2. [Code and artifact repositories](https://govstack-global.atlassian.net/wiki/spaces/GH/pages/377946151/Source+code+repository)
2. Mifos Payment Hub as Payment Building Block
   1. to be inserted
3. iGrant.io as Consent Building Block
   1. to be inserted
4. OpenIMIS as Digital Registries Building Block
   1. [Deployment Instructions](https://openimis.atlassian.net/wiki/spaces/OP/pages/589463708/Generic+Implementation+Starter+Kit)
   2. [Code and artifact repositories](https://github.com/GovStackWorkingGroup/sandbox-bb-digital-registries/tree/main/digital-registries/open-imis)
5. Building Block [Emulator ](../../explore-stack/building-blocks/emulators.md)

### Deploy Use Case Frontend and Backend

1. Deploy [Unconditional Social Cash Transfer (USCT) Backend](https://github.com/GovStackWorkingGroup/sandbox-usecase-usct-backend/blob/main/docs/main.md)
2. Deploy [Unconditional Social Cash Transfer (USCT) Frontend](https://github.com/GovStackWorkingGroup/sandbox-usecase-usct-frontend)

OR

Build your own Use Case [by following our example](../best-practice-example-design-of-the-sandbox-building-permit-use-case/)

## Struggling with setting up the prototype?

{% content-ref url="get-deployment-support.md" %}
[get-deployment-support.md](get-deployment-support.md)
{% endcontent-ref %}

