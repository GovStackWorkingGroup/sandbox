# Use Case Frontend

The Use Case Frontend is responsible for the interaction with the user (e.g. citizen or civil servant). The User Interface (UI) is visually and technically designed to ease understanding and usage of the displayed functionalities by users. The business logic is managed by the [Use Case Backend](use-case-backend.md).

## What do we use to <mark style="background-color:blue;">build</mark> it?

<table><thead><tr><th width="225">Name</th><th>Purpose</th></tr></thead><tbody><tr><td><a href="https://react.dev/">React</a></td><td>Library for web and native user interfaces</td></tr><tr><td><a href="https://vitejs.dev/">Vite</a></td><td>Developer tool</td></tr><tr><td><a href="https://chakra-ui.com/">Chakra-UI</a></td><td>Component library for bootstrapping (in USCT and Consturction Permit demo)</td></tr><tr><td>Material-UI</td><td>Component library for bootstrapping (in Early Warning demo)</td></tr></tbody></table>

## Where do we <mark style="background-color:blue;">demo</mark> it?

<table><thead><tr><th width="378">GitHub Repository</th><th>Used in...</th></tr></thead><tbody><tr><td><a href="https://github.com/GovStackWorkingGroup/sandbox-playground">USCT Frontend Application</a></td><td><a href="../access-demos/usct-use-case.md">Unconditional Social Cash Transfer (USCT) Demo</a><br><a href="https://www.govstack.global/our-offerings/govspecs/simulation/">Unconditional Social Cash Transfer (USCT) Simulation</a></td></tr><tr><td><a href="https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend">Construction Permit Frontend Application</a></td><td><a href="../access-demos/construction-permit-use-case.md">Construction Permit Use Case</a></td></tr><tr><td><a href="https://github.com/GovStackWorkingGroup/sandbox-usecase-earlywarning-frontend">Early Warning Frontend</a></td><td><a href="../access-demos/early-warning-tech-demo/">Early Warning Demo</a></td></tr></tbody></table>

## Which <mark style="background-color:blue;">conceptual decisions</mark> do we follow?

#### Early Warning Material-UI

React, a popular JavaScript library for building user interfaces, is the chosen frontend technology for the demo. When paired with Material UI, a robust component library that implements Google’s Material Design, it provides a powerful framework for creating responsive and visually appealing applications.

**Key Features**

* **Component-Based Architecture**: React’s component-based structure allows developers to build encapsulated components that manage their own state, promoting reusability and maintainability.
* **Declarative UI**: React enables developers to describe how the UI should look based on the current application state, making it easier to understand and debug.
* **Virtual DOM**: This feature optimizes rendering by updating only the parts of the UI that have changed, enhancing performance and user experience.

**Material UI Integration**

* **Pre-Built Components**: Material UI offers a wide range of pre-designed components, such as buttons, forms, and navigation elements, which adhere to Material Design principles. This accelerates development and ensures consistency across the application.
* **Customizability**: While providing a solid design foundation, Material UI allows for extensive customization, enabling developers to tailor components to meet specific branding and functional requirements.
* **Responsive Design**: The library supports responsive layouts, ensuring that applications look great on various devices, from desktops to mobile phones.

#### USCT Chakra-UI

Both the [full-stack USCT demo](../access-demos/usct-use-case.md) and the [front-end only USCT](https://www.govstack.global/our-offerings/govspecs/simulation/) demo applications live in the same application due to the interconnectedness of the UI and not seeing a point in separating them at this point in time for simplicity's sake. The full-stack demo is an MVP-like application demonstrating how the front-end and the back-end work together when using multiple building blocks to build an application.

#### The RPC Layer

The RPC Layer is based on the [Facade Pattern](https://en.wikipedia.org/wiki/Facade_pattern). In short, we are using it as a configurable API layer for the full-stack USCT demo. It allows us granular control over our API call method endpoints from one location, which is good for demonstrating connectivity between different interchangeable Building Blocks. In addition, the RPC layer can also be configured for different providers, such as MockProvider, APIProvider, LocalStorageProvider, etc.

## Further documentation

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Early Warning Frontend</strong></td><td>GitHub Repository</td><td></td><td><a href="../.gitbook/assets/github-6980894_640.png">github-6980894_640.png</a></td><td><a href="https://github.com/GovStackWorkingGroup/sandbox-usecase-earlywarning-frontend">https://github.com/GovStackWorkingGroup/sandbox-usecase-earlywarning-frontend</a></td></tr><tr><td><strong>USCT Use Case Frontend</strong></td><td>GitHub Repository</td><td></td><td><a href="../.gitbook/assets/github-6980894_640.png">github-6980894_640.png</a></td><td><a href="https://github.com/GovStackWorkingGroup/sandbox-playground">https://github.com/GovStackWorkingGroup/sandbox-playground</a></td></tr><tr><td><strong>Construction Permit Frontend</strong></td><td>GitHub Repository</td><td></td><td><a href="../.gitbook/assets/github-6980894_640.png">github-6980894_640.png</a></td><td><a href="https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend">https://github.com/GovStackWorkingGroup/sandbox-usecase-bp-frontend</a></td></tr></tbody></table>
