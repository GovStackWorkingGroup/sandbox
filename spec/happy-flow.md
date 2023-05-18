# Minimum Viable Product eg. Happy Flow

## Overview
The USCT MVP is built based upon the technical sandbox and the USCT simulation. It’s intended to enable a vertical
penetration (re-define vertical penetration) of GovStack based on a slice of the journey of the use case "Unconditional
Social Cash Transfer" in order to make a common exemplary journey accessible to all teams and groups. **It is a technical
proof of concept and example implementation for the GovStack community.**

![Happy-flow-circle](.gitbook/assets/circle.png)


## Steps

Steps are cover only minimum part of workflow and will use only some fragments from BB functionality, there will be 
no errors, corner cases and non-compliances, mocked authentication.

[Civil servant](terminology-abbreviations.md#civil-servant) will perform next steps:

```mermaid
sequenceDiagram


User ->> ID: Login
ID ->> MOCK SRIS: 
participant im as IM
User ->> Registry: Fetch
participant im. as IM
User ->> Payment: Register beneficiary
MOCK SRIS ->> Payment: Validate
MOCK SRIS ->> Payment: Trigger payment
MOCK SRIS ->> User: Result

```

### Login to the SRIS
Implementation should use one-time auth call by email. As a response user will get a token.

Implementation has two options: 

#### MOSIP
User will be verified (see [Identity and verification](https://govstack-global.atlassian.net/wiki/spaces/DEMO/pages/179896365/Identity+and+verification) )

[Documentation](https://docs.mosip.io/1.2.0/).

#### Mock identity system
Lightweight alternative for MOSIP.

[Definition](https://github.com/mosip/esignet-mock-services/tree/master/mock-identity-system) 

[API example](./login/api.md)

### Register citizen to SRIS (OpenIMIS)
When entering citizens personal ID, citizens personal data will be pulled and personal data fields filled automatically with mocked data in CR Citizen Registry (UNCTAD) (see [Registration](https://govstack-global.atlassian.net/wiki/spaces/DEMO/pages/179601480/Registration) ) 

### Link/choose benefit program to citizen
list of mocked programs is provided (OpenIMIS) (see  [Registration](https://govstack-global.atlassian.net/wiki/spaces/DEMO/pages/179601480/Registration) )

It should come from https://oleksii-1.gitbook.io/open-imis/2-api#provide-benefit-program-details-product-details  Provide Benefit program details (Product details) endpoint in OpenIMIS

### Registration
Add additional benefit related information (payment due date, payment amount, account no …) to the BOMS form (OpenIMIS) (see  [Registration](https://govstack-global.atlassian.net/wiki/spaces/DEMO/pages/179601480/Registration) )

### Submit benefit package to the citizen
Payment request triggered from OpenIMIS, which is background functionality.

Fill registration [form](https://govstack.gitbook.io/bb-registration/v/registration-1.0/7-service-apis#8.1-online-registration-e-services).

[Submit registration form](https://oleksii-1.gitbook.io/open-imis/2-api#request-beneficiary-enrollment) to OpenIMIS




### Payment 
Check if the payment due date is reached, trigger the benefit payment to the citizen by MIFOS functionality - this is the backround functionality, the verification of banc account is triggered towards IFMS mocked database (see [Payments](https://govstack-global.atlassian.net/wiki/spaces/DEMO/pages/179568721/Payments) )

#### Beneficiary onboarding
[API specification](https://govstack.gitbook.io/bb-payments/v/payments-1.0/9-service-apis#8.2.1-beneficiary-onboarding-api)

```json

{
  "RequestID": "system data", // 1
  "SourceBBID": "system data", // 2
  "Beneficiaries": [
    {
      "PayeeFunctionalID": "string", //3
      "PaymentModality": "string", //4
      "FinancialAddress": "string" //5 
    }
  ]
}
```
1. Globally unique ID which is coming from [driver app](happy-flow.md#implementation).
2. ID which is coming from [Information Mediator](https://github.com/GovStackWorkingGroup/sandbox-bb-information-mediator) to identify the origination of the request.
3. ID of the beneficiary.
4. Type of payment e.g. (Bank account, Mobile money...)
5. Financial address of the recipient of the cash transfer.

#### Prepayment validation request

API = https://govstack.gitbook.io/bb-payments/v/payments-1.0/9-service-apis#8.2.2-pre-payment-validation-api

#### OpenIMIS will create payment order


### Notification
Payment completed sent to the BOMS and Citizen - backround functionality will be mocked

## Implementation
Driver application building block is responsible to implement happy flow functionality.
Backend will call in order next building blocks APIs:
1. ID/MOSIP (optional)
2. UNCTAD
3. OpenIMIS
4. Payment