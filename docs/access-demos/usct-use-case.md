---
description: >-
  Demonstration of a full stack implementation using a Unconditional Social Cash
  Transfer (USCT) use case
---

# Social Cash Transfer Use Case

<img src="../.gitbook/assets/file.excalidraw.svg" alt="" class="gitbook-drawing">

Unconditional Social Cash Transfer (USCT) programs help families meet their basic needs for well-being and safety and serves as their path to self-sufficiency. USCT are cash payments provided to financially disadvantaged or vulnerable people or households without requiring anything in return (i.e. without conditionality).

This demo covers only a small fraction of a USCT user flow for the purpose of using various Building Block APIs. For a more comprehensive visualization of the use case visit the [GovStack USCT simulation](https://www.govstack.global/our-offerings/govspecs/simulation/).

## Which GovStack <mark style="background-color:blue;">features are demonstrated</mark>?

With this use case implementation, we demonstrate the GovStack approach through...

{% hint style="success" %}
**One possible way to implement the** [**GovStack Specifications**](https://govstack.gitbook.io/specification/)

Browse through all the stack components on the left-hand side menu, to explore the technical details on how we put the specifications into practice.
{% endhint %}

{% hint style="success" %}
**Interoperable Digital Public Infrastructure (DPI)**

GovStack Specification compliant and open source licensed

* BB Identity: MOSIP
* BB Payment: Mifos Payment Hub
* BB Information Mediator: X-Road
* BB Digital Registry: OpenIMIS
{% endhint %}

{% hint style="success" %}
**Architectural Best Practices**

* Different [Integration Scenarios](https://govstack.gitbook.io/specification/architecture-and-nonfunctional-requirements/6-onboarding) (native and via adapters)
* UI Switching (ID Authentication)
{% endhint %}

{% hint style="success" %}
**Reusable and Open Source**

Replicate the Frontend, Backend and Building Block (Emulators) or reuse specific components using our [DYI section](../follow-methodology/diy/).
{% endhint %}

{% hint style="success" %}
**Independent and automated Infrastructure and BB Deployment**

[Learn how we reduced dependency](../explore-stack/infrastructure.md) on one cloud provider and set-up continuous integration pipelines to ease managing building blocks software candidates.
{% endhint %}

## How to <mark style="background-color:blue;">access</mark>?

**Data Privacy Note:** By clicking on one of the access points you enter web applications operated by the Deutsche Gesellschaft für Internationale Zusammenarbeit (GIZ) GmbH where these Data Protection Notice and Registration Information are valid.

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td><strong>Social Cash Transfer Frontend</strong></td><td>Simplified steps of a civil servant user journey</td><td></td><td><a href="https://usct.dev.sandbox-playground.com/driver-poc/">https://usct.dev.sandbox-playground.com/driver-poc/</a></td><td><a href="../.gitbook/assets/USCT V2.png">USCT V2.png</a></td></tr></tbody></table>

{% hint style="warning" %}
Public UIs of other Building Blocks will be added until 15.01.2024
{% endhint %}

{% hint style="info" %}
This technical demo does not focus on user experience. For a the full user journey of this use case, visit our [GovStack Simulation](https://www.govstack.global/our-offerings/govspecs/simulation/).
{% endhint %}

### Use Case Frontend Walk Through

Registry Officer ID: `2371487382`\
Enrollment Officer ID: `5649650687`\
Payment Officer ID: `4893724702`\
OTP: `1 1 1 1 1 1`

Open the [Use Case Frontend](https://usct.dev.sandbox-playground.com/driver-poc/) and follow these steps to navigate through the demo.\
_In italic, read a very simplified version of the BB interactions._

<details>

<summary>Walk Through Steps</summary>

1. Click "Log in with e-signet"\
   _The user gets forwarded to the UI of the Identity BB. Demonstrating UI Switching_
2. Click "Log-in here" and enter the ID `5649650687` **to log in as Enrollment Office**
3. Enter `1 1 1 1 1 1` as One Time Password (OTP)
4. As fictional **Enrollment Officer give consent** to using essential personal information (You do not give consent to use your personal data! It is only for demonstration purposes.)\
   _The user gets forwarded back to the Use Case Frontend UI with respective role parameters<mark style="color:purple;">.</mark>_
5. Enter the "Candidate Database" and **enroll any person** to any available benefit package\
   _The user gets a list of candidates requested by the Use Case Backend from the Registry BB channeled through the Information Mediator BB._
6. After returning to the overview page, click on your profile in the top-right to **log out**\
   _The user triggers the Use Case Backend to request the Registry BB to change the enrollment status of a candidate._
7. Repeat the log in procedure with the ID `4893724702` **to log in as Payment Officer**\
   _Again, the user gets forwarded through the UI of the Identity BB._
8. Enter the "Beneficiary Database" and mark (check box) a person to **order payment**
9. Confirm Payment Order\
   _The user triggers the Use Case Backend to request the Payment BB to issue a payment order. They Payment BB returns successful execution of the payment._
10. Optional: Log in with the ID `2371487382` **to log in as Registry Officer** and **create new candidates.**

View a [sequence diagram describing all API requests between BB](https://github.com/GovStackWorkingGroup/sandbox-usecase-usct-backend/blob/main/docs/main.md) in the developer documentation

</details>

### Building Block UIs

Administrative UIs of the Building Block Software (X-Road, MOSIP, Mifos Payment Hub) can only be demonstrated by GovStack Initiative staff, until we implemented a secure way to expose the Admin UIs publicly. If you are interested, please [contact us](https://www.govstack.global/about/contact/).

## How are the stack components <mark style="background-color:blue;">assembled</mark>?

The following diagram shows one use case instance with used applications and Building Blocks.

<figure><img src="../explore-stack/assets/usct-govstack-instance.drawio.png" alt=""><figcaption></figcaption></figure>

For more details, browse through the high-level explanation component page or the in-depth documentation and code repositories of the various components.

<table><thead><tr><th width="283.6548980606663">Component Page</th><th>Developer Documentation</th><th>Code Repository</th></tr></thead><tbody><tr><td><a href="../explore-stack/use-case-frontend.md">Use Case Frontend</a></td><td></td><td><a href="https://github.com/GovStackWorkingGroup/sandbox-playground">USCT Frontend Repository</a></td></tr><tr><td><a href="../explore-stack/use-case-backend.md">Use Case Backend</a></td><td><a href="https://github.com/GovStackWorkingGroup/sandbox-usecase-usct-backend/blob/main/docs/main.md">USCT Backend Docs</a></td><td><a href="https://github.com/GovStackWorkingGroup/sandbox-usecase-usct-backend">USCT Backend Repository</a></td></tr><tr><td><a href="../explore-stack/building-blocks/">Building Blocks</a></td><td>X-Road</td><td>-</td></tr><tr><td></td><td>MOSIP</td><td><a href="https://github.com/tf-govstack">MOSIP Repository</a></td></tr><tr><td></td><td>Mifos</td><td>-</td></tr><tr><td></td><td>OpenIMIS + Adapter</td><td><a href="https://github.com/GovStackWorkingGroup/sandbox-bb-digital-registries/blob/main/digital-registries/open-imis/docs/1-main.md">OpenIMIS Repository</a></td></tr><tr><td><a href="../explore-stack/infrastructure.md">Infrastructure</a> &#x26; <a href="../explore-stack/devops.md">DevOps</a></td><td><a href="https://github.com/GovStackWorkingGroup/sandbox-infra/blob/main/docs/1-main.md">Infrastructure Docs</a></td><td><a href="https://github.com/GovStackWorkingGroup/sandbox-infra">Sandbox Infra Repository</a></td></tr></tbody></table>

***

## Data Protection Notice and Registration Information

The following information are valid for all web applications linked in the [access points chapter](usct-use-case.md#access-points).

<details>

<summary>Data Protection Notice</summary>

The Deutsche Gesellschaft für Internationale Zusammenarbeit (GIZ) GmbH attaches great importance to responsible and transparent management of personal data.

Below we provide users with information as to

* who they can contact at GIZ on the subject of data protection
* what data is processed when they visit the web application
* what rights they have with respect to us

**Controller and Data Protection Officer**

The responsible body for data processing is the Deutsche Gesellschaft für Internationale Zusammenarbeit (GIZ) GmbH.

Address:\
Friedrich-Ebert-Allee 32 + 36, 53113 Bonn\
Dag-Hammarskjöld-Weg 1–5, 65760 Eschborn

Contact:\
nico.lueck@giz.de

If you have specific questions about the protection of your data, please contact GIZ's data protection officer: datenschutzbeauftragte@giz.de

**General**

GIZ processes personal data exclusively in accordance with the [EU General Data Protection Regulation (GDPR)](https://eur-lex.europa.eu/legal-content/DE/TXT/PDF/?uri=CELEX:32016R0679\&qid=1527147390147\&from=EN) and the [German Federal Data Protection Act (Bundesdatenschutzgesetz, BDSG)](http://www.gesetze-im-internet.de/bdsg\_2018/index.html).\
Personal data are, for example, name, address, email addresses and user behaviour.

GIZ only processes personal data to the extent necessary. Which data is required and processed for which purpose and on what basis is largely determined by the type of service you use or the purpose for which the data is required.

**Cookies**

When you visit a web application, small text files, so-called cookies, are stored on your computer. They are used to make the online presence more user-friendly and effective overall Cookies cannot run programs or infect your computer with viruses.

The GIZ website uses cookies that are automatically deleted as soon as the browser in which the page is displayed is closed (so-called temporary cookies or session cookies). This type of cookie makes it possible to assign different requests from a browser to a session and to recognize the browser when you visit the website again (session ID).

**Collection of personal data when visiting a web application**

When visiting a [web application](usct-use-case.md#access-points), GIZ itself processes only the data that is automatically transmitted by the browser and technically required in order to display the website correctly and to ensure its stability and security. Each time a web application is accessed, the data stored includes, but is not limited to the following:

* Date (The date on which the activity occurred.)
* Time (The time, in coordinated universal time (UTC), at which the activity occurred.)
* Server IP Address (The IP address of the server on which the log file entry was generated.)
* Method (The requested action, for example, a GET method.)
* URI Stem (The target of the action, for example, Default.htm.)
* URI Query (The query, if any that the client was trying to perform. A Universal Resource Identifier (URI) query is necessary only for dynamic pages.)
* Server Port (The server port number that is configured for the service.)
* Client IP Address (The IP address of the client that made the request.)
* User Agent (The browser type that the client used.)
* Referrer (The site that the user last visited. This site provided a link to the current site.)
* HTTP Status (The HTTP status code.)
* Time Taken (The length of time that the action took, in milliseconds.)
* Request Body (The transmitted data for demonstration purposes (e.g. fictional person)

The data in the log file is temporary stored. The log retention time depend on amount of requests, service up time and other factors.

**Further information on the storage and transfer of data:**

GIZ is obliged to store data beyond the time of the visit in order to ensure protection against attacks on the GIZ’s internet infrastructure and the communications technology of the Federal Government (legal basis: Art. 6 (1) (e) GDPR in conjunction with Section 5 BSI Act). In the event of attacks on communications technology, this data is analyzed and used to initiate legal and criminal prosecution.

Data logged when accessing the GIZ's web applications is only transmitted to third parties if there is a legal obligation to do so or if the transmission is necessary for legal or criminal prosecution in the event of attacks on the Federal Government's communications technology. Data will not be passed on in any other cases. This data is not merged with other data sources at GIZ.

**Information on opting out**

Users who do not agree with the described processing of data cannot access the web applications. For technical reasons, opting out is not possible.

**Disclosure to third parties**

GIZ does not pass on personal data to third parties unless it is legally obliged or entitled to do so by law.

**Transfer of data to countries outside Germany**

GIZ does not transfer personal data to third countries. When using social media, the privacy policies of the respective providers apply.

**Duration of data retention**

User data will not be kept any longer than is necessary for the purpose for which it is processed or as required by law.

**IT security of user data**

GIZ accords great importance to protecting personal data. For this reason, technical and organisational security measures ensure that data is protected against accidental and intentional manipulation and unintended erasure as well as unauthorised access. These measures are updated accordingly based on technical developments and adapted continuously in line with the risks.

Visitors to the GIZ website have the right

* To obtain **information** about their data stored by us (Article 15 GDPR)
* To have their data stored by us **rectified** (Article 16 GDPR)
* To have their data stored by us **erased** (Article 17 GDPR)
* To obtain **restriction** of processing of their data stored by us (Article 18 GDPR)
* To **object** to the storage of their data if personal data are processed on the basis of the first sentence of Article 6 (1) 1 f and e GDPR (Article 21 GDPR)
* To receive their personal data in a commonly used and machine-readable format from the controller such that they can be potentially transmitted to another controller (right to **data portability**, Article 20 GDPR).
* To **withdraw** their consent to the extent that the data has been processed on the basis of consent (Article 6 (1) a GDPR). The lawfulness of the processing on the basis of the consent given remains unaffected until receipt of the withdrawal.

Users also have the right in accordance with Article 77 GDPR to **lodge a complaint with the competent data protection supervisory authority**. The competent authority is the Federal Commissioner for Data Protection and Freedom of Information ([BfDI](https://www.bfdi.bund.de/EN/Home/home\_node.html)).

</details>

<details>

<summary>Registration Information</summary>

Deutsche Gesellschaft für Internationale Zusammenarbeit (GIZ) GmbH

**Registered offices**

Bonn and Eschborn\
Germany

Friedrich-Ebert-Allee 32 + 36\
53113 Bonn\
Germany\
T +49 228 44 60-0\
F +49 228 44 60-17 66

Dag-Hammarskjöld-Weg 1 - 5\
65760 Eschborn\
Germany\
T +49 61 96 79-0\
F +49 61 96 79-11 15

E info@giz.de\
I www.giz.de

**Registered at**

Local court (Amtsgericht) Bonn, Germany: HRB 18384\
Local court (Amtsgericht) Frankfurt am Main, Germany: HRB 12394

**VAT no.**

DE 113891176

**Chairperson of the Supervisory Board**

Jochen Flasbarth, State Secretary in the Federal Ministry for Economic Cooperation and Development

**Management Board**

Thorsten Schäfer-Gümbel (Chair)\
Ingrid-Gabriela Hoven (Vice-Chair)\
Anna Sophie Herken

</details>
