# Use Case Frontend

The Use Case Frontend is responsible for the interaction with the user (e.g. citizen or civil servant). The User Interface (UI) is visually and technically designed to ease understanding and usage of the displayed functionalities by users. The business logic is managed by the [Use Case Backend](use-case-backend.md).

## What do we use to <mark style="background-color:blue;">build</mark> it?

<table><thead><tr><th width="225">Name</th><th>Purpose</th></tr></thead><tbody><tr><td><a href="https://react.dev/">React</a></td><td>Library for web and native user interfaces</td></tr><tr><td><a href="https://vitejs.dev/">Vite</a></td><td>Developer tool</td></tr><tr><td><a href="https://chakra-ui.com/">Chakra-UI</a></td><td>Component library for bootstrapping</td></tr></tbody></table>

For a deeper explanation of why these tools were chosen, read about the [Component Library Evaluation](https://govstack-global.atlassian.net/wiki/spaces/DEMO/pages/96043009/Component+Library+Evaluation) and [Front-end framework](https://govstack-global.atlassian.net/wiki/spaces/DEMO/pages/95912054/Frontend+Framework) on GovStack's Confluence.

## Where do we <mark style="background-color:blue;">demo</mark> it?

<table><thead><tr><th width="504">GitHub Repository</th><th>Used in...</th></tr></thead><tbody><tr><td><a href="https://github.com/GovStackWorkingGroup/sandbox-playground">USCT Frontend Application</a></td><td><a href="../access-demos/usct-use-case.md">USCT Use Case Demo</a><br><a href="https://www.govstack.global/our-offerings/govspecs/simulation/">USCT Use Case Simulation</a></td></tr><tr><td><a href="https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend">Construction Permit Frontend Application</a></td><td><a href="../access-demos/construction-permit-use-case.md">Construction Permit Use Case</a></td></tr></tbody></table>

## Which <mark style="background-color:blue;">conceptual decisions</mark> do we follow?

Both the [full-stack USCT demo](../access-demos/usct-use-case.md) and the [front-end only USCT](https://www.govstack.global/our-offerings/govspecs/simulation/) demo applications live in the same application due to the interconnectedness of the UI and not seeing a point in separating them at this point in time for simplicity's sake. The full-stack demo is an MVP-like application demonstrating how the front-end and the back-end work together when using multiple building blocks to build an application.

#### The RPC Layer

The RPC Layer is based on the [Facade Pattern](https://en.wikipedia.org/wiki/Facade\_pattern). In short, we are using it as a configurable API layer for the full-stack USCT demo. It allows us granular control over our API call method endpoints from one location, which is good for demonstrating connectivity between different interchangeable Building Blocks. In addition, the RPC layer can also be configured for different providers, such as MockProvider, APIProvider, LocalStorageProvider, etc.

## Further documentation

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>USCT Use Case Frontend</strong></td><td>GitHub Repository</td><td></td><td><a href="../.gitbook/assets/github-6980894_640.png">github-6980894_640.png</a></td><td><a href="https://github.com/GovStackWorkingGroup/sandbox-playground">https://github.com/GovStackWorkingGroup/sandbox-playground</a></td></tr><tr><td><strong>Construction Permit Frontend</strong></td><td>GitHub Repository</td><td></td><td><a href="../.gitbook/assets/github-6980894_640.png">github-6980894_640.png</a></td><td><a href="https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend">https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend</a></td></tr><tr><td></td><td></td><td></td><td></td><td></td></tr></tbody></table>
