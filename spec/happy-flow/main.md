# Minimum Viable Product (MVP) eg. Happy Flow

## Overview
Following page will cover USCT  (Unconditional Social Cash Transfer) minimum “Happy” flow and BB involvement in it. Minimum requirements from USCT MVP workflow perspective.

USCT description: [Digital Impact Exchange](https://solutions.dial.community/use_cases/unconditional_social_cash_transf) 

## Flow

### Login to the SRIS
Implementation should use one-time auth call by email. As a response user will get a token.

Implementation has two options:

#### MOSIP
User will be verified (see [Identity and verification](https://govstack-global.atlassian.net/wiki/spaces/DEMO/pages/179896365/Identity+and+verification) )

[Documentation](https://docs.mosip.io/1.2.0/).

#### Mock identity system
Lightweight alternative for MOSIP.

[Definition](https://github.com/mosip/esignet-mock-services/tree/master/mock-identity-system)

[API example](loginpi.md)

### Search form for entering citizen ID
Obtaining form data structure from registry BB.
```json
{
  "eFormId": "d98a205a-679b-485b-823d-7a32a391e744",
  "name": "A1",
  "description": "string",
  "version": "1",
  "latest": true,
  "schema": {
    "additionalProp1": {
      "FullName": "",
      "PersonalID": ""
      }
    }
  }

```