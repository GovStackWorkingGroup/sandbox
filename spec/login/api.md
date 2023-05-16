# API

```json
{
  "openapi": "3.1.0",
  "x-stoplight": {
    "id": "kz7t1w02vas7y"
  },
  "info": {
    "title": "mock-identity-system",
    "version": "1.0",
    "summary": "Mock Identity System mocks the few features of authentication system to provide a very simple integration example for IdP",
    "description": "Mock Identity System API will be used by demo applications to create and manage mock identities ",
    "contact": {
      "name": "MOSIP Team",
      "url": "https://www.mosip.io/",
      "email": "info@mosip.io"
    },
    "license": {
      "name": "MPL-2.0",
      "url": "https://www.mozilla.org/en-US/MPL/2.0/"
    }
  },
  "servers": [
    {
      "url": "https://api.collab.mosip.net/v1/mock-identity-system",
      "description": "collab"
    }
  ],
  "paths": {
    "/identity": {
      "parameters": [],
      "post": {
        "summary": "Add mock identity",
        "operationId": "post-mock-identity-individual-id",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "application/json": {
                "schema": {
                  "type": "object",
                  "properties": {
                    "responseTime": {
                      "type": "string"
                    },
                    "response": {
                      "type": "object",
                      "properties": {
                        "status": {
                          "type": "string"
                        }
                      },
                      "required": [
                        "status"
                      ]
                    },
                    "errors": {
                      "type": "array",
                      "items": {
                        "$ref": "#/components/schemas/Error"
                      }
                    }
                  },
                  "required": [
                    "responseTime"
                  ]
                },
                "examples": {
                  "Example 1": {
                    "value": {
                      "responseTime": "2022-12-09T12:24:46.481Z",
                      "response": {
                        "status": "ACTIVE"
                      },
                      "errors": []
                    }
                  }
                }
              }
            }
          }
        },
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "type": "object",
                "properties": {
                  "requestTime": {
                    "type": "string"
                  },
                  "request": {
                    "$ref": "#/components/schemas/Identity"
                  }
                },
                "required": [
                  "requestTime",
                  "request"
                ]
              },
              "examples": {
                "Example 1": {
                  "value": {
                    "individualId": "8267411575",
                    "pin": "55555",
                    "fullName": [
                      {
                        "language": "fra",
                        "value": "Alice"
                      },
                      {
                        "language": "ara",
                        "value": "أليس"
                      },
                      {
                        "language": "eng",
                        "value": "Alice"
                      }
                    ],
                    "gender": [
                      {
                        "language": "eng",
                        "value": "Female"
                      },
                      {
                        "language": "fra",
                        "value": "Femâle"
                      },
                      {
                        "language": "ara",
                        "value": "ذكر"
                      }
                    ],
                    "dateOfBirth": "1995/07/02",
                    "streetAddress": [
                      {
                        "language": "fra",
                        "value": "yuān⥍"
                      },
                      {
                        "language": "ara",
                        "value": "$لُنگᆑ"
                      },
                      {
                        "language": "eng",
                        "value": "Slung"
                      }
                    ],
                    "locality": [
                      {
                        "language": "fra",
                        "value": "CMâttye"
                      },
                      {
                        "language": "ara",
                        "value": "دسييسيكدك"
                      },
                      {
                        "language": "eng",
                        "value": "Cmattey"
                      }
                    ],
                    "region": [
                      {
                        "language": "fra",
                        "value": "melh$pèng"
                      },
                      {
                        "language": "ara",
                        "value": "مِله$پِ̀نگ"
                      },
                      {
                        "language": "eng",
                        "value": "melhspeng"
                      }
                    ],
                    "postalCode": "45009",
                    "country": [
                      {
                        "language": "fra",
                        "value": "India"
                      },
                      {
                        "language": "ara",
                        "value": "الهند"
                      },
                      {
                        "language": "eng",
                        "value": "India"
                      }
                    ],
                    "encodedPhoto": "dhdfhdhhdhdfhfdh==",
                    "individualBiometrics": {
                      "format": "cbeff",
                      "version": 1,
                      "value": "dhdfhdhhdhdfhfdh=="
                    },
                    "phone": "+919427357935",
                    "email": "alice1234@gmail.com"
                  }
                }
              }
            }
          }
        },
        "description": "Persist the mock identity in database and returns the status",
        "tags": [
          "mock-identity"
        ]
      }
    },
    "/identity/{individualId}": {
      "get": {
        "summary": "Get mock identity",
        "tags": [
          "mock-identity"
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "application/json": {
                "schema": {
                  "type": "object",
                  "properties": {
                    "responseTime": {
                      "type": "string"
                    },
                    "response": {
                      "$ref": "#/components/schemas/Identity"
                    },
                    "errors": {
                      "type": "array",
                      "items": {
                        "$ref": "#/components/schemas/Error"
                      }
                    }
                  },
                  "required": [
                    "responseTime"
                  ]
                },
                "examples": {
                  "Example 1": {
                    "value": {
                      "individualId": "8267411575",
                      "pin": "55555",
                      "fullName": [
                        {
                          "language": "fra",
                          "value": "Alice"
                        },
                        {
                          "language": "ara",
                          "value": "أليس"
                        },
                        {
                          "language": "eng",
                          "value": "Alice"
                        }
                      ],
                      "gender": [
                        {
                          "language": "eng",
                          "value": "Female"
                        },
                        {
                          "language": "fra",
                          "value": "Femâle"
                        },
                        {
                          "language": "ara",
                          "value": "ذكر"
                        }
                      ],
                      "dateOfBirth": "1995/07/02",
                      "streetAddress": [
                        {
                          "language": "fra",
                          "value": "yuān⥍"
                        },
                        {
                          "language": "ara",
                          "value": "$لُنگᆑ"
                        },
                        {
                          "language": "eng",
                          "value": "Slung"
                        }
                      ],
                      "locality": [
                        {
                          "language": "fra",
                          "value": "CMâttye"
                        },
                        {
                          "language": "ara",
                          "value": "دسييسيكدك"
                        },
                        {
                          "language": "eng",
                          "value": "Cmattey"
                        }
                      ],
                      "region": [
                        {
                          "language": "fra",
                          "value": "melh$pèng"
                        },
                        {
                          "language": "ara",
                          "value": "مِله$پِ̀نگ"
                        },
                        {
                          "language": "eng",
                          "value": "melhspeng"
                        }
                      ],
                      "postalCode": "45009",
                      "country": [
                        {
                          "language": "fra",
                          "value": "India"
                        },
                        {
                          "language": "ara",
                          "value": "الهند"
                        },
                        {
                          "language": "eng",
                          "value": "India"
                        }
                      ],
                      "encodedPhoto": "dhdfhdhhdhdfhfdh==",
                      "individualBiometrics": {
                        "format": "cbeff",
                        "version": 1,
                        "value": "dhdfhdhhdhdfhfdh=="
                      },
                      "phone": "+919427357935",
                      "email": "alice1234@gmail.com"
                    }
                  }
                }
              }
            }
          }
        },
        "operationId": "get-mock-identity",
        "description": "Returns the mock identity belonging to the individual id"
      },
      "parameters": [
        {
          "schema": {
            "type": "string"
          },
          "name": "individualId",
          "in": "path",
          "required": true,
          "description": "Individual id of the foundation id system"
        }
      ]
    }
  },
  "components": {
    "schemas": {
      "Identity": {
        "type": "object",
        "x-examples": {
          "Example 1": {
            "individualId": "8267411572",
            "pin": "55555",
            "gender": [
              {
                "language": "eng",
                "value": "Female"
              },
              {
                "language": "fra",
                "value": "Femâle"
              },
              {
                "language": "ara",
                "value": "ذكر"
              }
            ],
            "city": [
              {
                "language": "fra",
                "value": "CMâttye"
              },
              {
                "language": "ara",
                "value": "دسييسيكدك"
              },
              {
                "language": "eng",
                "value": "Cmattey"
              }
            ],
            "postalCode": "45009",
            "fullName": [
              {
                "language": "fra",
                "value": "Himaja Dhanya R"
              },
              {
                "language": "ara",
                "value": "تتگلدكنسَزقهِقِفل دسييسيكدكنوڤو"
              },
              {
                "language": "eng",
                "value": "Himaja Dhanya R"
              }
            ],
            "dateOfBirth": "1995/07/02",
            "individualBiometrics": null,
            "province": [
              {
                "language": "fra",
                "value": "Kénitra"
              },
              {
                "language": "ara",
                "value": "كِ́نِترَ"
              },
              {
                "language": "eng",
                "value": "Kénitra"
              }
            ],
            "zone": [
              {
                "language": "fra",
                "value": "Ben Mansour"
              },
              {
                "language": "ara",
                "value": "بِن مَنسُُر"
              },
              {
                "language": "eng",
                "value": "Ben Mansour"
              }
            ],
            "phone": "+919427357935",
            "addressLine1": [
              {
                "language": "fra",
                "value": "yuān⥍"
              },
              {
                "language": "ara",
                "value": "$لُنگᆑ"
              },
              {
                "language": "eng",
                "value": "Slung"
              }
            ],
            "addressLine2": [
              {
                "language": "fra",
                "value": "yuān 2"
              },
              {
                "language": "ara",
                "value": "يَُانꉛ⥍"
              },
              {
                "language": "eng",
                "value": "yuan wee"
              }
            ],
            "addressLine3": [
              {
                "language": "fra",
                "value": "yuān 3"
              },
              {
                "language": "ara",
                "value": "$لُنگᆑ"
              },
              {
                "language": "eng",
                "value": "yuan wee 3"
              }
            ],
            "region": [
              {
                "language": "fra",
                "value": "melh$pèng"
              },
              {
                "language": "ara",
                "value": "مِله$پِ̀نگ"
              },
              {
                "language": "eng",
                "value": "melhspeng"
              }
            ],
            "email": "dhanya.himaja@gmail.com",
            "encodedPhoto": "dhdfhdhhdhdfhfdh=="
          }
        },
        "examples": [
          {
            "individualId": "8267411575",
            "pin": "55555",
            "fullName": [
              {
                "language": "fra",
                "value": "Alice"
              },
              {
                "language": "ara",
                "value": "أليس"
              },
              {
                "language": "eng",
                "value": "Alice"
              }
            ],
            "gender": [
              {
                "language": "eng",
                "value": "Female"
              },
              {
                "language": "fra",
                "value": "Femâle"
              },
              {
                "language": "ara",
                "value": "ذكر"
              }
            ],
            "dateOfBirth": "1995/07/02",
            "streetAddress": [
              {
                "language": "fra",
                "value": "yuān⥍"
              },
              {
                "language": "ara",
                "value": "$لُنگᆑ"
              },
              {
                "language": "eng",
                "value": "Slung"
              }
            ],
            "locality": [
              {
                "language": "fra",
                "value": "CMâttye"
              },
              {
                "language": "ara",
                "value": "دسييسيكدك"
              },
              {
                "language": "eng",
                "value": "Cmattey"
              }
            ],
            "region": [
              {
                "language": "fra",
                "value": "melh$pèng"
              },
              {
                "language": "ara",
                "value": "مِله$پِ̀نگ"
              },
              {
                "language": "eng",
                "value": "melhspeng"
              }
            ],
            "postalCode": "45009",
            "country": [
              {
                "language": "fra",
                "value": "India"
              },
              {
                "language": "ara",
                "value": "الهند"
              },
              {
                "language": "eng",
                "value": "India"
              }
            ],
            "encodedPhoto": "dhdfhdhhdhdfhfdh==",
            "individualBiometrics": {
              "format": "cbeff",
              "version": 1,
              "value": "dhdfhdhhdhdfhfdh=="
            },
            "phone": "+919427007935",
            "email": "alice1234@gmail.com"
          }
        ],
        "properties": {
          "individualId": {
            "type": "string"
          },
          "pin": {
            "type": "string"
          },
          "fullName": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/LanguageValue"
            }
          },
          "gender": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/LanguageValue"
            }
          },
          "dateOfBirth": {
            "type": "string"
          },
          "streetAddress": {
            "type": "array",
            "description": "Full street address component, which MAY include house number, street name, Post Office Box, and multi-line extended street address information. This field MAY contain multiple lines, separated by newlines. ",
            "items": {
              "$ref": "#/components/schemas/LanguageValue"
            }
          },
          "locality": {
            "type": "array",
            "description": "City or locality component",
            "items": {
              "$ref": "#/components/schemas/LanguageValue"
            }
          },
          "region": {
            "type": "array",
            "description": "State, province, prefecture, or region component.",
            "items": {
              "$ref": "#/components/schemas/LanguageValue"
            }
          },
          "postalCode": {
            "type": "string",
            "description": "Zip code or postal code component."
          },
          "country": {
            "type": "array",
            "description": "Country name component",
            "items": {
              "$ref": "#/components/schemas/LanguageValue"
            }
          },
          "encodedPhoto": {
            "type": "string"
          },
          "individualBiometrics": {
            "$ref": "#/components/schemas/Biometrics"
          },
          "email": {
            "type": "string"
          },
          "phone": {
            "type": "string"
          }
        },
        "required": [
          "individualId",
          "pin",
          "fullName",
          "gender",
          "dateOfBirth",
          "streetAddress",
          "locality",
          "region",
          "postalCode",
          "encodedPhoto",
          "email",
          "phone"
        ]
      },
      "LanguageValue": {
        "type": "object",
        "x-examples": {
          "Example 1": {
            "language": "eng",
            "value": "Female"
          }
        },
        "properties": {
          "language": {
            "type": "string"
          },
          "value": {
            "type": "string"
          }
        },
        "required": [
          "language",
          "value"
        ]
      },
      "Biometrics": {
        "type": "object",
        "x-examples": {
          "Example 1": {
            "format": "cbeff",
            "version": 1,
            "value": "individualBiometrics_bio_CBEFF"
          }
        },
        "properties": {
          "format": {
            "type": "string"
          },
          "version": {
            "type": "integer"
          },
          "value": {
            "type": "string"
          }
        },
        "required": [
          "format",
          "version",
          "value"
        ]
      },
      "Error": {
        "description": "",
        "type": "object",
        "properties": {
          "errorCode": {
            "type": "string",
            "minLength": 1
          },
          "message": {
            "type": "string",
            "minLength": 1
          }
        },
        "required": [
          "errorCode",
          "message"
        ],
        "x-examples": {
          "example-1": {
            "errorCode": "RES-SER-29",
            "message": "Invalid id::No Record(s) found"
          }
        }
      }
    }
  }
}
```