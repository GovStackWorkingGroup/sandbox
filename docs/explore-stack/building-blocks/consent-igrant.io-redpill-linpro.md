---
description: >-
  Information on the software solution based on iGrant.io and Redpill Linpro
  which we selected as the Consent Building Block
---

# Consent: iGrant.io/Redpill Linpro

{% embed url="https://www.youtube.com/watch?v=UAiFvciYM34" %}

## Functional Scope

The Consent Building Block (BB) empowers individuals to approve the use of their data using a comprehensive framework encompassing laws, norms and principles, system architectures and standards. The word consent embraces all lawful bases in this context. It can interchangeably be used to mean a data agreement. A consent agreement is a data agreement with a lawful basis of “consent”.&#x20;

This innovative solution addresses the needs of organisations engaged in personal data processing, enabling them to respect individual preferences and lawfully manage their data. It covers all lawful bases of processing to conform with data protection regulations. Operating as a process-driven element within the GovStack BB ecosystem, the Consent BB orchestrates transparent data agreements while seamlessly integrating with various other BBs.

All features listed in the specification have been implemented. The key features and functionalities are summarised below:

### Organisation admin features for configurations

<table data-header-hidden><thead><tr><th width="232"></th><th></th></tr></thead><tbody><tr><td>Manage Data Agreement (Consent Agreement)</td><td>The Administrator can perform all CRUD operations. This includes viewing, updating, and downloading a data agreement as a JSON file and deleting a published data agreement.</td></tr><tr><td>Personal data</td><td>The Administrator can view all data processed in the organisation defined in the data agreement. This is read-only.</td></tr><tr><td>Manage consents</td><td>The Administrator can manage end-user consents.</td></tr><tr><td>Consent records</td><td>The Administrator can view consents and use filters, etc.</td></tr><tr><td>Subscription</td><td>The Administrator can onboard existing Individuals (subscribers) to the organisation. This is useful for legacy applications.</td></tr><tr><td>Privacy dashboard</td><td>The Administrator can configure and deploy the privacy dashboard via this panel.</td></tr><tr><td>Account</td><td>The Administrator can manage accounts in the Consent BB using this panel.</td></tr><tr><td>Manage admin</td><td>The Administrator can manage user accounts, passwords, etc., via this panel.</td></tr><tr><td>Developer APIs</td><td>Organisations can view the endpoints, tokens, etc, here.</td></tr><tr><td>View logs</td><td>The Administrator can view all administrative logs via this panel.</td></tr><tr><td>Webhooks</td><td>Here, the Administrator can configure webhooks.</td></tr></tbody></table>

### Individual features

| Data Agreement / Consent ON/OFF | With this feature, the individual can lawfully toggle ON/OFF those data agreements with lawful basis consent. |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| Data sharing                    | Any real-time data sharing will leverage enhanced OAuth-based consent based on data agreements.               |

## Architecture

The Consent BB software employs a microservice architecture, leveraging container technology to create self-contained, independently deployable software components. These components facilitate high availability, resilience and service continuity by allowing deployment on Docker for development and Kubernetes for production, ensuring no single point of failure through multi-instance deployment and database clustering. A reverse proxy directs traffic, enabling seamless interaction with client applications. The architecture supports rolling software upgrades to maintain continuous service availability, minimising the risk of downtime.

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption><p>Consent BB microservice reference end-to-end architecture</p></figcaption></figure>

The Consent BB encompasses several software elements crucial for its operation. It includes a user interface (UI) for both desktop and mobile platforms, a backend microservice with RESTful APIs for interaction, and a database to ensure data persistence. The architecture also includes an administrative dashboard for managing data agreements and auditing user consent. In Figure 02, key backend components are highlighted, with core components in blue and optional modules in pink. The API server acts as a bridge between user-facing components and the backend, using RESTful APIs for communication. A significant gap is the need for integrated IAM (identity and access management) for user authentication, even though IAM plays a crucial role in such ecosystems.

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption><p>Software component architecture of Consent BB</p></figcaption></figure>

## Technology Stack

All software servers and web UI components are generally dockerised, Kubernetes is used for orchestration, RESTful APIs are used for communication, and microservices architecture is used for system design. The various technologies used within Consent BB software components are summarised in the table below:

<table><thead><tr><th width="265">Software Component</th><th>Technologies used</th></tr></thead><tbody><tr><td>User Interfaces (Organisation)</td><td></td></tr><tr><td>Admin Dashboard</td><td>React.js, CSS and Typescript</td></tr><tr><td>Data Sharing UI</td><td>React.js, CSS and Typescript</td></tr><tr><td>User Interfaces (Individual Privacy Dashboard)</td><td></td></tr><tr><td>WebClient</td><td>React.js, CSS and Typescript</td></tr><tr><td>Android SDK</td><td>Kotlin and SDK are distributed through Jitpack repository</td></tr><tr><td>iOS SDK</td><td>Swift and SDK are distributed through Cocoapods</td></tr><tr><td>APIs</td><td>Documented using OpenAPI specification 3.0</td></tr><tr><td>Consent BB server backend</td><td>Go, Bash scripts are distributed as Docker containers through the Docker hub. MongoDB is used for the database, and Keycloak is for the IAM.</td></tr></tbody></table>

The project uses a modern and flexible technology stack to achieve its goals efficiently. Docker and Kubernetes are employed for containerisation and orchestration, ensuring scalability and ease of deployment. RESTful APIs are used for communication between various components, promoting interoperability and flexibility in system design. A microservices architecture further enhances the system's scalability, maintainability, and resilience.&#x20;

React.js, CSS, and Typescript are chosen for the user interfaces, offering a robust and responsive front-end development environment. These technologies enable the creation of dynamic and user-friendly interfaces for organisational and individual privacy dashboards.&#x20;

The project leverages Kotlin for Android SDK and Swift for iOS SDK for mobile development. These languages are well-suited for mobile app development, providing high-performance and native user experiences. The distribution of SDKs through the Jitpack repository and Cocoapods simplifies integration and management for developers.&#x20;

Regarding backend development, Go is selected for the Consent BB server backend. Go is a lightweight and efficient programming language for building scalable and concurrent applications. Bash scripts are used for automation tasks, enhancing the deployment and maintenance processes.

For data storage, MongoDB is chosen for its flexibility and scalability, allowing the system to handle large volumes of data efficiently. Keycloak is used for identity and access management (IAM), ensuring secure authentication and authorisation processes.&#x20;

Overall, the technology stack selected for the Consent building block project reflects a strategic choice to leverage modern, efficient, and scalable technologies to deliver a robust and secure system for managing consent and privacy.

## Key Considerations for Implementation

### For decision-makers

Legal compliance and ethics

* Review and adhere to local and international data protection laws and regulations (e.g., GDPR in the European Union).
* Ensure ethical considerations are paramount, prioritising user consent and the right to privacy. A data protection impact assessment (DPIA) is strongly recommended before formulating the data agreements.

Transparency and user trust

* Communicate the purpose, scope, and duration of data collection and processing transparently. Follow practices as per ISO27560 in this regard.&#x20;

Data minimisation and purpose limitation

* Collect and process only the strictly necessary data for the defined purpose.
* Provide a purpose description that is easy to understand from an end-user/individual perspective.
* Limit data access and processing to the specified purposes for which consent was given.

Security and data protection

* Implement robust security measures to protect personal data from unauthorised access, alteration, or destruction.
* Regularly review and update security protocols and encryption methods.

Individual control and accessibility

* Enable users to access, review, and manage their consent settings easily.
* Provide mechanisms towards individuals, as laid out in the Consent BB solution, to withdraw consent anytime, ensuring a straightforward process

Integration and interoperability

* Ensure the Consent BB integrates seamlessly with other GovStack BBs and existing systems.
* Adopt standards that support interoperability and data portability between different services and platforms.

&#x20;Monitoring, evaluation, and adaptation

* Establish mechanisms for ongoing monitoring and evaluation of the consent management system’s effectiveness.
* Be prepared to adapt and update consent practices and technology in response to evolving legal standards, technological advancements and user expectations.

Stakeholder engagement and collaboration

Engage with a wide range of stakeholders, including users, data protection authorities, and civil society organisations, to ensure the Consent BB meets the needs and expectations of all parties. By considering these aspects, decision-makers can ensure that the implementation of the GovStack Consent BB not only complies with legal requirements but also fosters trust and transparency, effectively safeguarding users' rights and data.

### For architects

GovStack’s Consent BB is designed as modular microservices exposed as RESTful APIs, and application architects should focus on ensuring the seamless integration, secure implementation and efficient operation of these services within the broader ecosystem. Here are the key considerations for application architects working with such a system:

Integration strategy

* Define clear integration points between the Consent BB and existing applications, focusing on API endpoints, data exchange formats and communication protocols.
* Utilise API gateways and service meshes to manage, secure and monitor service interactions.

Data management and privacy&#x20;

Assuming that a DPIA is carried out to formulate the data agreements, implement advanced signing capability while toggling consents in enhanced logging and auditing capabilities to track consent changes and access personal data, supporting transparency and accountability.

User experience and accessibility

* Integrating the Consent BB privacy dashboard into existing individual interfaces is highly recommended. Also, Consent BB integrates seamlessly into user workflows, ensuring that consent mechanisms are intuitive, accessible and non-disruptive.
* Provide clear information and controls to users, allowing them to manage their consent preferences easily

Scalability and performance

* Ensure that the deployment can scale to meet demand, leveraging container orchestration tools for dynamic scaling.
* Optimise performance to handle high volumes of consent checks and updates without impacting user experience or system responsiveness.&#x20;

Focusing on these considerations will help architects incorporate the Consent BB into their existing IT applications, ensuring a secure, compliant and user-friendly implementation.

## Code Repositories

* [Software Component Repository User Interfaces (Organisation) Admin Dashboard](https://github.com/decentralised-dataexchange/bb-consent-admin-dashboard)&#x20;
* [User Interfaces (Individual Privacy Dashboard) WebClient ](https://github.com/decentralised-dataexchange/bb-consent-privacy-dashboard)
* [Android SDK](https://github.com/decentralised-dataexchange/bb-consent-android-privacy-dashboard)
* [iOS SDK](https://github.com/decentralised-dataexchange/bb-consent-ios-privacy-dashboard) &#x20;
* [APIs](https://consent-bb-swagger.igrant.io/v2023.11.1/index.html#get-/service/verification/consent-records)
* [Consent BB server backend](https://github.com/decentralised-dataexchange/bb-consent-api)
* [Data4Diabetes Demo App](https://github.com/decentralised-dataexchange/data4diabetes-app)
