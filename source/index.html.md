---
title: API Reference

language_tabs:
  - php
  - ruby
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Wicket API! You can use our API to access Wicket API endpoints, which can get information on various people, orders, and associated membership details from the Wicket database.

We have language bindings for PHP, Ruby, and Javascript! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Slate](https://github.com/tripit/slate). Feel free to edit it and use it as a base for your own API's documentation.

# Authentication

> To authorize, use this code:

```ruby
require 'wicket'

api = Wicket::API.authorize!('meowmeowmeow')
```

```php

```

```javascript
const wicket = require('wicket');

let api = wicket.authorize('meowmeowmeow');
```

> Make sure to replace `meowmeowmeow` with your API key.

Wicket uses API keys to allow access to the API. You can register a new Wicket API key at our [developer portal](http://example.com/developers).

Wicket expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

# People

## Get All People

```ruby
require 'Wicket'

api = Wicket::API.authorize!('meowmeowmeow')
api.people.get
```

```php

```

```javascript
const wicket = require('wicket');

let api = wicket.authorize('meowmeowmeow');
let people = api.people.get();
```

> The above command returns JSON structured like this:

```json
{
  "data": [
    {
      "id": "aabc65ce-3de9-4ab2-8fb3-0b032a2e25b7",
      "type": "people",
      "attributes": {
        "uuid": "aabc65ce-3de9-4ab2-8fb3-0b032a2e25b7",
        "given_name": "Rakhi",
        "family_name": ".",
        "additional_name": null,
        "alternate_name": "Rakhi .",
        "slug": "rakhi",
        "gender": "female",
        "honorific_prefix": "Ms.",
        "honorific_suffix": null,
        "job_title": "physical therapist",
        "birth_date": "1982-08-25",
        "created_at": "2015-08-21T13:44:29.000Z",
        "updated_at": "2016-09-26T18:16:59.547Z",
        "deleted_at": null,
        "language": "en",
        "membership_action": [
          "addon"
        ],
        "membership_number": "2030350",
        "membership_began_on": "2015-11-13",
        "tags": [],
        "data": {
          "license": {
            "resource_id": "3c3099aa-01f0-46c0-b1a7-dcf40b4e1b22",
            "registration_number": "7335"
          },
          "companyid": 87191,
          "education": {
            "resource_id": "IN",
            "resource_type": "countries",
            "graduation_year": "2005"
          },
          "employment": {
            "sector": "Private",
            "primary": "GPPC"
          },
          "comp_idcust": "2030350",
          "member_since": "2015-11-13",
          "communications": {
            "email": true,
            "email_third_party": true
          }
        },
        "role_names": [
          "user",
          "member"
        ],
        "user": {
          "email": "physiorakhi1982@gmail.com",
          "username": "physiorakhi1982@gmail.com",
          "reset_password_sent_at": null,
          "confirmation_sent_at": "2016-08-04T23:15:30.457Z",
          "confirmed_at": null
        }
      },
      "relationships": {
        "organizations": {
          "data": [
            {
              "id": "c1519a7d-6abc-42e1-bc9b-1f6d1f586e6f",
              "type": "organizations"
            }
          ],
          "meta": {
            "pivot": [
              {
                "id": "c1519a7d-6abc-42e1-bc9b-1f6d1f586e6f",
                "type": "Practising B"
              }
            ]
          }
        },
        "phones": {
          "data": [
            {
              "id": "2c28fbf6-8e74-4ada-92a1-407e2ae31016",
              "type": "phones"
            }
          ]
        },
        "emails": {
          "data": [
            {
              "id": "acbd3643-03a8-4032-8afc-189e6db88c6e",
              "type": "emails"
            }
          ]
        },
        "addresses": {
          "data": [
            {
              "id": "f8786f9d-e58b-4cee-b728-e648602c62c4",
              "type": "addresses"
            }
          ]
        },
        "orders": {
          "data": [
            {
              "id": "c735ebd3-5004-4892-8d95-d741cc1394bd",
              "type": "orders"
            },
            {
              "id": "199b8c3e-7bef-4752-9dc6-8c3399767f57",
              "type": "orders"
            }
          ]
        },
        "identities": {
          "data": [
            {
              "id": "71163856-6d50-4a0d-b595-eb9fa7b68ad1",
              "type": "identities"
            }
          ]
        },
        "comments": {
          "data": []
        },
        "groups": {
          "data": []
        },
        "images": {
          "data": []
        },
        "documents": {
          "data": []
        },
        "touchpoints": {
          "data": [
            {
              "id": "c5d61ade-b8c9-47dd-93ab-c6797ba5931d",
              "type": "touchpoints"
            },
            {
              "id": "b215412b-f480-4975-8060-42012109882c",
              "type": "touchpoints"
            }
          ]
        },
        "roles": {
          "data": [
            {
              "id": "74b8d086-3a73-4ce3-b0ec-528b6fe348c0",
              "type": "roles"
            },
            {
              "id": "a3f41f64-a5e6-4db2-81b2-b9d5285ee9eb",
              "type": "roles"
            }
          ]
        },
        "received_messages": {
          "data": [
            {
              "id": "93ce9f01-1cf3-4998-b5f2-1dae856d6bf9",
              "type": "messages"
            },
            {
              "id": "f7f3278d-72d3-4d09-a9a1-a6ad5002d8d6",
              "type": "messages"
            }
          ]
        },
        "sent_messages": {
          "data": []
        }
      }
    }
  }
}
```

This endpoint retrieves all people.

### HTTP Request

`GET http://example.com/api/people`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
organization_id | null | If set, it will scope the results to specific organizations.
q | null | A set of query parameters used to filter/sort results. Expanded in the parameters section.
page[number] | null | Return the specific page of results.
page[size] | 25 | Number of entries to return per page.

## Get a Specific Person

```ruby
require 'wicket'

api = Wicket::API.authorize!('meowmeowmeow')
api.person.get('8fa80837-35a3-48f3-a2a0-89b1e0ee6ad4')
```

```php

```

```javascript
const wicket = require('wicket');

let api = wicket.authorize('meowmeowmeow');
let max = api.person.get('8fa80837-35a3-48f3-a2a0-89b1e0ee6ad4');
```

> The above command returns JSON structured like this:

```json
{
  "data": {
    "id": "77ede037-e8a2-4602-8c82-91c810ff657d",
    "type": "people",
    "attributes": {
      "uuid": "77ede037-e8a2-4602-8c82-91c810ff657d",
      "given_name": "Derek",
      "family_name": "Ethier",
      "additional_name": null,
      "alternate_name": "Derek Ethier",
      "slug": "derek-ethier",
      "gender": "unselected",
      "honorific_prefix": null,
      "honorific_suffix": null,
      "job_title": null,
      "birth_date": "1991-03-11",
      "created_at": "2016-08-04T22:24:38.808Z",
      "updated_at": "2016-08-04T22:24:38.808Z",
      "deleted_at": null,
      "language": "en",
      "membership_action": [
        "renew"
      ],
      "membership_number": "486033",
      "membership_began_on": "2016-08-04",
      "tags": [],
      "data": {
        "communications": {
          "email": true,
          "email_third_party": true
        }
      },
      "current_membership_summary": {
        "state": [
          "eligible"
        ],
        "order_id": null,
        "order_type": null,
        "order_completed_at": null,
        "interval": {
          "uuid": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
          "name_en": "CPA Annual Membership 2016",
          "name_fr": "ACP Adhésion Annuelle 2016",
          "previous_uuid": "580e479f-c374-4fb7-bd0d-a63fe0751258"
        }
      },
      "available_membership_summaries": [],
      "previous_membership_summaries": [
        {
          "state": [
            "present"
          ],
          "order_id": null,
          "order_type": null,
          "order_completed_at": null,
          "interval": {
            "uuid": "580e479f-c374-4fb7-bd0d-a63fe0751258",
            "name_en": "CPA Annual Membership 2015",
            "name_fr": "ACP Adhésion Annuelle 2015",
            "previous_uuid": "e29a6337-438d-4340-a7b6-87b7e7918f49"
          },
          "root_membership": {
            "name_en": "Practising A",
            "description_en": null,
            "name_fr": null,
            "description_fr": null,
            "number": "486033",
            "code": "FFT"
          }
        }
      ],
      "role_names": [
        "user",
        "administrator"
      ],
      "user": {
        "email": "dethier@industrialagency.ca",
        "username": "dethier",
        "reset_password_sent_at": null,
        "confirmation_sent_at": null,
        "confirmed_at": "2016-08-04T00:00:00.000Z"
      }
    },
    "relationships": {
      "pending_membership_orders": {
        "data": []
      },
      "organizations": {
        "data": [
          {
            "id": "b41af38f-86af-4c7e-a6fa-25e87e7b9200",
            "type": "organizations"
          },
          {
            "id": "9dd5a3bf-68fd-418f-812f-bf4d3818f9e0",
            "type": "organizations"
          }
        ],
        "meta": {
          "pivot": [
            {
              "id": "c1519a7d-6abc-42e1-bc9b-1f6d1f586e6f",
              "type": "FOC"
            },
            {
              "id": "b41af38f-86af-4c7e-a6fa-25e87e7b9200",
              "type": null
            }
          ]
        }
      },
      "phones": {
        "data": []
      },
      "emails": {
        "data": [
          {
            "id": "ab4aeb16-d8c7-4f20-813b-7107c7927f34",
            "type": "emails"
          }
        ]
      },
      "addresses": {
        "data": []
      },
      "orders": {
        "data": []
      },
      "identities": {
        "data": [
          {
            "id": "9c210f04-9693-4430-94e3-3d8792ca6302",
            "type": "identities"
          }
        ]
      },
      "comments": {
        "data": []
      },
      "groups": {
        "data": []
      },
      "images": {
        "data": []
      },
      "documents": {
        "data": []
      },
      "touchpoints": {
        "data": [
          {
            "id": "ad96f247-c619-41f9-8f13-8cc40de2a0c5",
            "type": "touchpoints"
          },
          {
            "id": "a803e00f-57e8-4c78-9e41-046de736f5a9",
            "type": "touchpoints"
          }
        ]
      },
      "roles": {
        "data": [
          {
            "id": "74b8d086-3a73-4ce3-b0ec-528b6fe348c0",
            "type": "roles"
          },
          {
            "id": "4bcd322b-24b6-4cea-afbc-fa61557d1644",
            "type": "roles"
          }
        ]
      },
      "received_messages": {
        "data": [
          {
            "id": "67ff9abb-dc9f-4d4b-95bf-ae7d2a13cf9f",
            "type": "messages"
          },
          {
            "id": "98e0594b-b1ce-49f3-b72b-fe0ff3956379",
            "type": "messages"
          }
        ]
      },
      "sent_messages": {
        "data": [
          {
            "id": "90bef392-a61f-4934-b22a-f0abc2e75d26",
            "type": "messages"
          },
          {
            "id": "dd7064da-bec9-4959-bdae-d6a4f61ad163",
            "type": "messages"
          }
        ]
      },
      "leaves": {
        "data": []
      }
    }
  },
  "included": [
    {
      "id": "b41af38f-86af-4c7e-a6fa-25e87e7b9200",
      "type": "organizations",
      "attributes": {
        "uuid": "b41af38f-86af-4c7e-a6fa-25e87e7b9200",
        "alternate_name": "BC",
        "legal_name": "Physiotherapy Association of British Columbia (PABC)",
        "description": "Physiotherapy Association of British Columbia (PABC)",
        "slug": "physiotherapy-association-of-british-columbia-pabc",
        "ancestry": "1",
        "duns": null,
        "people_count": 2315,
        "created_at": "2016-08-04T22:24:03.323Z",
        "updated_at": "2016-08-04T22:24:09.360Z",
        "deleted_at": null,
        "type": "branch",
        "inheritable_from_parent": [
          "memberships"
        ],
        "inherits_from_parent": {
          "memberships": true
        },
        "tags": []
      },
      "relationships": {
        "phones": {
          "data": []
        },
        "emails": {
          "data": []
        },
        "addresses": {
          "data": []
        },
        "memberships": {
          "data": [
            {
              "id": "4d040d82-d284-4eab-8a27-7d8219c27085",
              "type": "memberships"
            },
            {
              "id": "15c270ab-2491-42d2-ae51-959ed4dae6e9",
              "type": "memberships"
            }
          ]
        },
        "insurance_options": {
          "data": []
        },
        "payment_methods": {
          "data": []
        },
        "comments": {
          "data": []
        },
        "groups": {
          "data": [
            {
              "id": "7b63d2f2-314d-43eb-8259-a3800c098082",
              "type": "groups"
            },
            {
              "id": "aed6312b-a470-4774-af65-f58a5cb08f77",
              "type": "groups"
            }
          ]
        },
        "roles": {
          "data": [
            {
              "id": "5a705c5e-26fe-4549-b7ad-ee1a6a25d209",
              "type": "roles"
            },
            {
              "id": "c04db1ec-5f78-4da1-bd30-102acf9404bb",
              "type": "roles"
            }
          ]
        }
      },
      "meta": {
        "ancestry_depth": 1
      }
    },
    {
      "id": "9dd5a3bf-68fd-418f-812f-bf4d3818f9e0",
      "type": "organizations",
      "attributes": {
        "uuid": "9dd5a3bf-68fd-418f-812f-bf4d3818f9e0",
        "alternate_name": "ON",
        "legal_name": "Ontario Physiotherapy Association (OPA)",
        "description": "Ontario Physiotherapy Association (OPA)",
        "slug": "ontario-physiotherapy-association-opa",
        "ancestry": "1",
        "duns": null,
        "people_count": 4978,
        "created_at": "2016-08-04T22:24:03.417Z",
        "updated_at": "2016-08-04T22:24:21.884Z",
        "deleted_at": null,
        "type": "branch",
        "inheritable_from_parent": [
          "memberships"
        ],
        "inherits_from_parent": {
          "memberships": true
        },
        "tags": []
      },
      "relationships": {
        "phones": {
          "data": []
        },
        "emails": {
          "data": []
        },
        "addresses": {
          "data": []
        },
        "memberships": {
          "data": [
            {
              "id": "eefaf32f-767b-43d4-9807-3b0073c34ee5",
              "type": "memberships"
            },
            {
              "id": "6a79b539-f66f-4fe2-b431-699dc80e8570",
              "type": "memberships"
            }
          ]
        },
        "insurance_options": {
          "data": []
        },
        "payment_methods": {
          "data": []
        },
        "comments": {
          "data": []
        },
        "groups": {
          "data": [
            {
              "id": "cb8c70c8-97f0-42d3-af86-fe8ba04f2b74",
              "type": "groups"
            },
            {
              "id": "fb143266-0ccf-4e38-9814-6702fb7be891",
              "type": "groups"
            }
          ]
        },
        "roles": {
          "data": [
            {
              "id": "9b8adc93-cfcd-48f6-892b-c3c4b66faa30",
              "type": "roles"
            },
            {
              "id": "8d24b2d7-250f-46f7-b442-c5028f5075cd",
              "type": "roles"
            },
            {
              "id": "ef406d3a-799a-4cb4-8664-ca927672a901",
              "type": "roles"
            }
          ]
        }
      },
      "meta": {
        "ancestry_depth": 1
      }
    },
    {
      "id": "e4c31066-41d6-4007-8ca0-79e94d5d2c95",
      "type": "organizations",
      "attributes": {
        "uuid": "e4c31066-41d6-4007-8ca0-79e94d5d2c95",
        "alternate_name": "DIVSRS",
        "legal_name": "Seniors' Health",
        "description": "Seniors' Health",
        "slug": "seniors-health",
        "ancestry": "1",
        "duns": null,
        "people_count": 1160,
        "created_at": "2016-08-04T22:24:03.693Z",
        "updated_at": "2016-08-04T22:24:03.693Z",
        "deleted_at": null,
        "type": "division",
        "inheritable_from_parent": [
          "memberships"
        ],
        "inherits_from_parent": {},
        "tags": []
      },
      "relationships": {
        "phones": {
          "data": []
        },
        "emails": {
          "data": []
        },
        "addresses": {
          "data": []
        },
        "memberships": {
          "data": [
            {
              "id": "3e2a6373-c40d-4f1a-93c1-5507d5cb0319",
              "type": "memberships"
            }
          ]
        },
        "insurance_options": {
          "data": []
        },
        "payment_methods": {
          "data": []
        },
        "comments": {
          "data": []
        },
        "groups": {
          "data": []
        },
        "roles": {
          "data": [
            {
              "id": "b07456d2-4ec3-4aad-be83-26f4da23d95f",
              "type": "roles"
            }
          ]
        }
      },
      "meta": {
        "ancestry_depth": 1
      }
    },
    {
      "id": "0ad024b2-9f34-434a-a8a8-7f9a545bd991",
      "type": "organizations",
      "attributes": {
        "uuid": "0ad024b2-9f34-434a-a8a8-7f9a545bd991",
        "alternate_name": "DIVPPD",
        "legal_name": "Private Practice",
        "description": "Private Practice",
        "slug": "private-practice",
        "ancestry": "1",
        "duns": null,
        "people_count": 1775,
        "created_at": "2016-08-04T22:24:03.676Z",
        "updated_at": "2016-08-04T22:24:03.676Z",
        "deleted_at": null,
        "type": "division",
        "inheritable_from_parent": [
          "memberships"
        ],
        "inherits_from_parent": {},
        "tags": []
      },
      "relationships": {
        "phones": {
          "data": []
        },
        "emails": {
          "data": []
        },
        "addresses": {
          "data": []
        },
        "memberships": {
          "data": [
            {
              "id": "f1b891a6-c1c3-4483-b2f1-97d26d54e579",
              "type": "memberships"
            }
          ]
        },
        "insurance_options": {
          "data": []
        },
        "payment_methods": {
          "data": []
        },
        "comments": {
          "data": []
        },
        "groups": {
          "data": []
        },
        "roles": {
          "data": [
            {
              "id": "4dce7276-82e9-4dab-bbcd-4166e13ad202",
              "type": "roles"
            }
          ]
        }
      },
      "meta": {
        "ancestry_depth": 1
      }
    },
    {
      "id": "c1519a7d-6abc-42e1-bc9b-1f6d1f586e6f",
      "type": "organizations",
      "attributes": {
        "uuid": "c1519a7d-6abc-42e1-bc9b-1f6d1f586e6f",
        "alternate_name": "CPA",
        "legal_name": "Canadian Physiotherapy Association",
        "description": "Canadian Professionals in Physiotherapy",
        "slug": "canadian-physiotherapy-association",
        "ancestry": null,
        "duns": null,
        "people_count": 17329,
        "created_at": "2016-08-04T22:24:03.273Z",
        "updated_at": "2016-08-04T22:24:03.273Z",
        "deleted_at": null,
        "type": null,
        "inheritable_from_parent": [
          "memberships"
        ],
        "inherits_from_parent": {},
        "tags": []
      },
      "relationships": {
        "phones": {
          "data": []
        },
        "emails": {
          "data": []
        },
        "addresses": {
          "data": []
        },
        "memberships": {
          "data": [
            {
              "id": "4a42f5cb-0393-4e47-91bb-b36b845e80c3",
              "type": "memberships"
            },
            {
              "id": "1da0ce51-6d56-4383-a8d2-f621ac92882a",
              "type": "memberships"
            }
          ]
        },
        "insurance_options": {
          "data": [
            {
              "id": "fe9745bc-2dd7-4a54-8675-012cec644cd1",
              "type": "insurance_options"
            },
            {
              "id": "ed272f23-edba-4e1f-89b8-c7959dc51cb6",
              "type": "insurance_options"
            }
          ]
        },
        "payment_methods": {
          "data": [
            {
              "id": "b8bcce0b-5155-4c19-a36c-a1d7fdabbea9",
              "type": "payment_methods"
            },
            {
              "id": "8d35ae76-115a-4660-9047-375b2dc673f7",
              "type": "payment_methods"
            }
          ]
        },
        "comments": {
          "data": []
        },
        "groups": {
          "data": []
        },
        "roles": {
          "data": [
            {
              "id": "af07e489-7a2c-44bb-8b21-16190b3cfac3",
              "type": "roles"
            },
            {
              "id": "cc94b821-400e-4f47-bfef-e9c3d6bd58dc",
              "type": "roles"
            }
          ]
        }
      },
      "meta": {
        "ancestry_depth": 0
      }
    },
    {
      "id": "ab4aeb16-d8c7-4f20-813b-7107c7927f34",
      "type": "emails",
      "attributes": {
        "uuid": "ab4aeb16-d8c7-4f20-813b-7107c7927f34",
        "localpart": "dethier",
        "domain": "industrialagency.ca",
        "type": "work",
        "created_at": "2016-08-04T22:24:38.818Z",
        "updated_at": "2016-08-04T22:24:38.818Z",
        "deleted_at": null,
        "address": "dethier@industrialagency.ca",
        "primary": true
      },
      "relationships": {
        "emailable": {
          "data": {
            "id": "77ede037-e8a2-4602-8c82-91c810ff657d",
            "type": "people"
          }
        },
        "organization": {
          "data": null
        }
      }
    },
    {
      "id": "74b8d086-3a73-4ce3-b0ec-528b6fe348c0",
      "type": "roles",
      "attributes": {
        "uuid": "74b8d086-3a73-4ce3-b0ec-528b6fe348c0",
        "name": "user",
        "description": null,
        "slug": "user"
      },
      "relationships": {
        "resource": {
          "data": null
        }
      }
    },
    {
      "id": "4bcd322b-24b6-4cea-afbc-fa61557d1644",
      "type": "roles",
      "attributes": {
        "uuid": "4bcd322b-24b6-4cea-afbc-fa61557d1644",
        "name": "administrator",
        "description": null,
        "slug": "administrator-9681a9cf-56b8-409c-b911-60bde22ce04b"
      },
      "relationships": {
        "resource": {
          "data": null
        }
      }
    }
  ]
}
```

This endpoint retrieves a specific person.

### HTTP Request

`GET http://example.com/people/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the person to retrieve (UUID)

# Orders

## Get All Orders

```ruby
require 'Wicket'

api = Wicket::API.authorize!('meowmeowmeow')
api.orders.get
```

```php

```

```javascript
const wicket = require('wicket');

let api = wicket.authorize('meowmeowmeow');
let people = api.orders.get();
```

> The above command returns JSON structured like this:

```json
{
  "data": [
    {
      "id": "4ee22704-05d4-4c52-8c25-677a16883764",
      "type": "orders",
      "attributes": {
        "uuid": "4ee22704-05d4-4c52-8c25-677a16883764",
        "type": "renew",
        "state": "completed",
        "number": "M258384935",
        "item_total": "575.0",
        "adjustment_total": "-575.0",
        "manual_adjustment_total": "0.0",
        "included_tax_total": "0.0",
        "additional_tax_total": "0.0",
        "tax_total": "0.0",
        "promotion_total": "-575.0",
        "interval_total": "0.0",
        "leave_total": "0.0",
        "subtotal": "0.0",
        "total": "0.0",
        "payment_total": "0.0",
        "total_refunded": "0.0",
        "total_refundable": "0.0",
        "ip_address": "54.237.157.10",
        "locale": "fr",
        "completed_at": "2016-10-18T15:35:00.738Z",
        "updated_at": "2016-10-18T15:35:01.837Z",
        "created_at": "2016-10-18T15:34:32.614Z",
        "order_steps": [
          "profile",
          "membership",
          "preferences",
          "insurance",
          "addon",
          "review",
          "donation",
          "payment",
          "payment_pending",
          "completed",
          "refunding",
          "refunded"
        ],
        "order_steps_progress": [
          "profile",
          "membership",
          "preferences",
          "insurance",
          "addon",
          "review",
          "donation",
          "payment"
        ],
        "available_order_steps": [
          "refunding",
          "refunded"
        ],
        "number_of_payments": 0,
        "outstanding_balance": "0.0",
        "number_of_remaining_payments": 0,
        "first_payment_amount": "0.0",
        "recurring_payment_amount": 0,
        "last_payment_amount": 0,
        "next_payment_amount": "0.0",
        "next_payment_date": "2016-11-15T00:00:00.000Z",
        "in_progress": false,
        "refundable": false,
        "can_add_manual_payments": false,
        "data": {
          "insurance_answers": {
            "interested": {
              "option": "0",
              "details": null
            },
            "renewing_existing": {
              "option": "0",
              "details": null
            },
            "insurance_start_date": "2016-10-18"
          },
          "membership_answers": {
            "license": null,
            "education": null
          },
          "previous_order_uuid": "3088dd42-2991-4f9c-ad59-053b111383ea",
          "previous_membership_codes": [
            "STD",
            "DIVACU",
            "DIVCAR",
            "DIVONC",
            "DIVLEAD",
            "DIVOPD",
            "DIVNEU",
            "DIVSRS",
            "DIVPPD",
            "DIVWHD",
            "DIVPAIN",
            "DIVSPC",
            "DIVARD",
            "DIVIHD",
            "DIVPED",
            "QC"
          ],
          "bypass_license_education_validation": true
        }
      },
      "relationships": {
        "person": {
          "data": {
            "id": "6fd574b1-4772-45ad-a238-1ee466f312ac",
            "type": "people"
          }
        },
        "interval": {
          "data": {
            "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
            "type": "intervals"
          }
        },
        "billing_address": {
          "data": null
        },
        "tax_address": {
          "data": {
            "id": "ab5445e3-5010-44c3-9b0c-83dcafb80d66",
            "type": "addresses"
          }
        },
        "payment_option": {
          "data": null
        },
        "payment_method": {
          "data": null
        },
        "payment_options": {
          "data": [
            {
              "id": "4ee057c2-4a32-4b35-8ea9-2454302d656f",
              "type": "payment_options"
            },
            {
              "id": "087e15b6-83aa-4ab8-92e8-17f4985d1104",
              "type": "payment_options"
            }
          ]
        },
        "payment_methods": {
          "data": []
        },
        "state_changes": {
          "data": [
            {
              "id": "94762",
              "type": "state_changes"
            }
          ]
        },
        "line_items": {
          "data": [
            {
              "id": "802fc626-756d-48e7-9b7f-d0355f5ad1b3",
              "type": "line_items"
            },
            {
              "id": "3c0ad488-ef1c-471e-beb2-ccd4045da6f6",
              "type": "line_items"
            }
          ]
        },
        "payments": {
          "data": []
        },
        "refunds": {
          "data": []
        },
        "adjustments": {
          "data": []
        },
        "documents": {
          "data": []
        },
        "intervals": {
          "data": [
            {
              "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
              "type": "intervals"
            }
          ]
        },
        "available_variants": {
          "links": {
            "related": "/orders/4ee22704-05d4-4c52-8c25-677a16883764/available_variants"
          }
        }
      }
    }
  }
}
```

This endpoint retrieves all orders.

### HTTP Request

`GET http://example.com/api/orders`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
q | null | A set of query parameters used to filter/sort results. Expanded in the parameters section.
page[number] | null | Return the specific page of results.
page[size] | 25 | Number of entries to return per page.

## Get A Specific Order

```ruby
require 'Wicket'

api = Wicket::API.authorize!('meowmeowmeow')
api.orders.get('d8b5792d-3487-4694-b6b2-a812f0498032')
```

```php

```

```javascript
const wicket = require('wicket');

let api = wicket.authorize('meowmeowmeow');
let people = api.orders.get('d8b5792d-3487-4694-b6b2-a812f0498032');
```

> The above command returns JSON structured like this:

```json
{
  "data": {
    "id": "4ee22704-05d4-4c52-8c25-677a16883764",
    "type": "orders",
    "attributes": {
      "uuid": "4ee22704-05d4-4c52-8c25-677a16883764",
      "type": "renew",
      "state": "completed",
      "number": "M258384935",
      "item_total": "575.0",
      "adjustment_total": "-575.0",
      "manual_adjustment_total": "0.0",
      "included_tax_total": "0.0",
      "additional_tax_total": "0.0",
      "tax_total": "0.0",
      "promotion_total": "-575.0",
      "interval_total": "0.0",
      "leave_total": "0.0",
      "subtotal": "0.0",
      "total": "0.0",
      "payment_total": "0.0",
      "total_refunded": "0.0",
      "total_refundable": "0.0",
      "ip_address": "54.237.157.10",
      "locale": "fr",
      "completed_at": "2016-10-18T15:35:00.738Z",
      "updated_at": "2016-10-18T15:35:01.837Z",
      "created_at": "2016-10-18T15:34:32.614Z",
      "order_steps": [
        "profile",
        "membership",
        "preferences",
        "insurance",
        "addon",
        "review",
        "donation",
        "payment",
        "payment_pending",
        "completed",
        "refunding",
        "refunded"
      ],
      "order_steps_progress": [
        "profile",
        "membership",
        "preferences",
        "insurance",
        "addon",
        "review",
        "donation",
        "payment"
      ],
      "available_order_steps": [
        "refunding",
        "refunded"
      ],
      "number_of_payments": 0,
      "outstanding_balance": "0.0",
      "number_of_remaining_payments": 0,
      "first_payment_amount": "0.0",
      "recurring_payment_amount": 0,
      "last_payment_amount": 0,
      "next_payment_amount": "0.0",
      "next_payment_date": "2016-11-15T00:00:00.000Z",
      "in_progress": false,
      "refundable": false,
      "can_add_manual_payments": false,
      "data": {
        "insurance_answers": {
          "interested": {
            "option": "0",
            "details": null
          },
          "renewing_existing": {
            "option": "0",
            "details": null
          },
          "insurance_start_date": "2016-10-18"
        },
        "membership_answers": {
          "license": null,
          "education": null
        },
        "previous_order_uuid": "3088dd42-2991-4f9c-ad59-053b111383ea",
        "previous_membership_codes": [
          "STD",
          "DIVACU",
          "DIVCAR",
          "DIVONC",
          "DIVLEAD",
          "DIVOPD",
          "DIVNEU",
          "DIVSRS",
          "DIVPPD",
          "DIVWHD",
          "DIVPAIN",
          "DIVSPC",
          "DIVARD",
          "DIVIHD",
          "DIVPED",
          "QC"
        ],
        "bypass_license_education_validation": true
      },
      "message_codes": [
        {
          "state": "base",
          "code": "is_renewal"
        }
      ],
      "step_validation_messages": null
    },
    "relationships": {
      "person": {
        "data": {
          "id": "6fd574b1-4772-45ad-a238-1ee466f312ac",
          "type": "people"
        }
      },
      "interval": {
        "data": {
          "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
          "type": "intervals"
        }
      },
      "billing_address": {
        "data": null
      },
      "tax_address": {
        "data": {
          "id": "ab5445e3-5010-44c3-9b0c-83dcafb80d66",
          "type": "addresses"
        }
      },
      "payment_option": {
        "data": null
      },
      "payment_method": {
        "data": null
      },
      "payment_options": {
        "data": [
          {
            "id": "4ee057c2-4a32-4b35-8ea9-2454302d656f",
            "type": "payment_options"
          },
          {
            "id": "087e15b6-83aa-4ab8-92e8-17f4985d1104",
            "type": "payment_options"
          }
        ]
      },
      "payment_methods": {
        "data": []
      },
      "state_changes": {
        "data": [
          {
            "id": "94762",
            "type": "state_changes"
          }
        ]
      },
      "line_items": {
        "data": [
          {
            "id": "802fc626-756d-48e7-9b7f-d0355f5ad1b3",
            "type": "line_items"
          },
          {
            "id": "3c0ad488-ef1c-471e-beb2-ccd4045da6f6",
            "type": "line_items"
          },
          {
            "id": "04aa2762-a00c-46af-b1c5-627e13019a68",
            "type": "line_items"
          },
          {
            "id": "f1d53497-9ce8-42a0-a9ad-8572a79e09c8",
            "type": "line_items"
          },
          {
            "id": "0f5d0989-d8f5-42c4-94ea-a08258640f07",
            "type": "line_items"
          },
          {
            "id": "21d48987-7a66-4f8e-97f7-f043ceca63ad",
            "type": "line_items"
          },
          {
            "id": "4d5eb8b6-5f23-4dbe-b087-b8f0dc7f147c",
            "type": "line_items"
          },
          {
            "id": "6a2bc618-42f5-428e-8c0a-adf374826637",
            "type": "line_items"
          },
          {
            "id": "0dd5ebb0-cddc-4209-9fa5-e174b7180f60",
            "type": "line_items"
          },
          {
            "id": "2d83093e-81a1-4877-adca-b7ca0f84ea18",
            "type": "line_items"
          },
          {
            "id": "f2a6dbe5-ce1e-4c8e-8a7d-0d41de019eb9",
            "type": "line_items"
          },
          {
            "id": "113ab3c0-bea6-40c4-b660-ad335eaf4831",
            "type": "line_items"
          },
          {
            "id": "c6eb6e25-9402-4b27-be26-e557ae88f9ef",
            "type": "line_items"
          },
          {
            "id": "833569cc-630a-4e02-acfb-8ad2c1350a14",
            "type": "line_items"
          },
          {
            "id": "bf1a4795-8260-4c58-b860-5c3843b44a5a",
            "type": "line_items"
          },
          {
            "id": "da7adaa8-2a18-4b9e-ba72-5c8c26f73318",
            "type": "line_items"
          }
        ]
      },
      "payments": {
        "data": []
      },
      "refunds": {
        "data": []
      },
      "adjustments": {
        "data": []
      },
      "documents": {
        "data": []
      },
      "intervals": {
        "data": [
          {
            "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
            "type": "intervals"
          }
        ]
      },
      "available_variants": {
        "links": {
          "related": "/orders/4ee22704-05d4-4c52-8c25-677a16883764/available_variants"
        }
      }
    }
  },
  "included": [
    {
      "id": "6fd574b1-4772-45ad-a238-1ee466f312ac",
      "type": "people",
      "attributes": {
        "uuid": "6fd574b1-4772-45ad-a238-1ee466f312ac",
        "given_name": "Léa",
        "family_name": "Couture Fernandez",
        "additional_name": null,
        "alternate_name": "Léa Couture Fernandez",
        "slug": "lea-couture-fernandez",
        "gender": "female",
        "honorific_prefix": "Madame",
        "honorific_suffix": null,
        "job_title": "",
        "birth_date": "1992-12-17",
        "created_at": "2015-10-05T17:49:09.000Z",
        "updated_at": "2016-08-05T09:53:56.930Z",
        "deleted_at": null,
        "language": "fr",
        "membership_action": [
          "upgrade",
          "addon"
        ],
        "membership_number": "2030014",
        "membership_began_on": "2015-10-06",
        "tags": [],
        "data": {
          "companyid": 88663,
          "education": null,
          "comp_idcust": "2030014",
          "member_since": "2015-10-06",
          "communications": {
            "email": true,
            "email_third_party": true
          }
        },
        "role_names": [
          "user",
          "member",
          "member",
          "member",
          "member",
          "member",
          "member",
          "member",
          "member",
          "member",
          "member",
          "member",
          "member",
          "member",
          "member",
          "member",
          "member"
        ],
        "user": {
          "email": "leacouturefernandez@hotmail.com",
          "username": "leacouturefernandez@hotmail.com",
          "reset_password_sent_at": "2016-08-08T15:00:10.860Z",
          "confirmation_sent_at": "2016-08-04T23:19:50.304Z",
          "confirmed_at": "2016-08-09T05:43:52.739Z"
        }
      },
      "relationships": {
        "organizations": {
          "data": [
            {
              "id": "0ca44da5-9379-4857-8d58-79c4d4c6be4c",
              "type": "organizations"
            },
            {
              "id": "1a59fe59-2338-493c-9448-ca66b2ffe36f",
              "type": "organizations"
            },
            {
              "id": "713b27f9-80d6-4134-a2fc-b33ae5075990",
              "type": "organizations"
            },
            {
              "id": "a8a73389-a08b-45e1-b23c-d044538cf15f",
              "type": "organizations"
            },
            {
              "id": "c7fdbba9-3e11-4584-ac96-bf9ed3c3a26c",
              "type": "organizations"
            },
            {
              "id": "98bc4e01-5f43-44d5-8e17-bb93d9318244",
              "type": "organizations"
            },
            {
              "id": "e4c31066-41d6-4007-8ca0-79e94d5d2c95",
              "type": "organizations"
            },
            {
              "id": "0ad024b2-9f34-434a-a8a8-7f9a545bd991",
              "type": "organizations"
            },
            {
              "id": "4ab31af8-9e82-4167-b5ee-c98ff2946743",
              "type": "organizations"
            },
            {
              "id": "15eabcee-7eed-4f03-9d9e-0d3ebf14e4ed",
              "type": "organizations"
            },
            {
              "id": "c5b5a920-ea36-49e5-a6d2-2be98b508cc2",
              "type": "organizations"
            },
            {
              "id": "30c94e30-10a9-4893-892b-c0ca07f68169",
              "type": "organizations"
            },
            {
              "id": "4a2bdaff-009a-4bdd-8615-ad02fc5a75ff",
              "type": "organizations"
            },
            {
              "id": "677f785b-331e-4fde-a7cc-65a8248e62db",
              "type": "organizations"
            },
            {
              "id": "d28b4645-d7b7-4c19-a9b2-15c6a5823ed1",
              "type": "organizations"
            },
            {
              "id": "c1519a7d-6abc-42e1-bc9b-1f6d1f586e6f",
              "type": "organizations"
            }
          ],
          "meta": {
            "pivot": [
              {
                "id": "c1519a7d-6abc-42e1-bc9b-1f6d1f586e6f",
                "type": null
              },
              {
                "id": "0ca44da5-9379-4857-8d58-79c4d4c6be4c",
                "type": null
              },
              {
                "id": "1a59fe59-2338-493c-9448-ca66b2ffe36f",
                "type": null
              },
              {
                "id": "c5b5a920-ea36-49e5-a6d2-2be98b508cc2",
                "type": null
              },
              {
                "id": "713b27f9-80d6-4134-a2fc-b33ae5075990",
                "type": null
              },
              {
                "id": "30c94e30-10a9-4893-892b-c0ca07f68169",
                "type": null
              },
              {
                "id": "c7fdbba9-3e11-4584-ac96-bf9ed3c3a26c",
                "type": null
              },
              {
                "id": "98bc4e01-5f43-44d5-8e17-bb93d9318244",
                "type": null
              },
              {
                "id": "a8a73389-a08b-45e1-b23c-d044538cf15f",
                "type": null
              },
              {
                "id": "677f785b-331e-4fde-a7cc-65a8248e62db",
                "type": null
              },
              {
                "id": "4a2bdaff-009a-4bdd-8615-ad02fc5a75ff",
                "type": null
              },
              {
                "id": "15eabcee-7eed-4f03-9d9e-0d3ebf14e4ed",
                "type": null
              },
              {
                "id": "0ad024b2-9f34-434a-a8a8-7f9a545bd991",
                "type": null
              },
              {
                "id": "e4c31066-41d6-4007-8ca0-79e94d5d2c95",
                "type": null
              },
              {
                "id": "d28b4645-d7b7-4c19-a9b2-15c6a5823ed1",
                "type": null
              },
              {
                "id": "4ab31af8-9e82-4167-b5ee-c98ff2946743",
                "type": null
              }
            ]
          }
        },
        "phones": {
          "data": [
            {
              "id": "813f82ed-1757-4ece-8f2a-90e37fb74829",
              "type": "phones"
            },
            {
              "id": "37a0343f-aa92-4863-9e37-a925b1a48bbb",
              "type": "phones"
            }
          ]
        },
        "emails": {
          "data": [
            {
              "id": "3fe03be2-d08d-4f11-9c8d-253766d86035",
              "type": "emails"
            }
          ]
        },
        "addresses": {
          "data": [
            {
              "id": "b79c135e-4eb6-4e65-9765-672369c47721",
              "type": "addresses"
            }
          ]
        },
        "orders": {
          "data": [
            {
              "id": "3088dd42-2991-4f9c-ad59-053b111383ea",
              "type": "orders"
            },
            {
              "id": "4ee22704-05d4-4c52-8c25-677a16883764",
              "type": "orders"
            }
          ]
        },
        "identities": {
          "data": [
            {
              "id": "d10c1761-c02a-4a4b-a6d9-d49cb72bb035",
              "type": "identities"
            },
            {
              "id": "27a0001c-7eb9-4864-951a-c9539f31dd6e",
              "type": "identities"
            },
            {
              "id": "034da914-eb10-45f5-ade6-f8137cc68552",
              "type": "identities"
            },
            {
              "id": "9782df0b-cdca-4c41-aa6b-d71609edf60d",
              "type": "identities"
            },
            {
              "id": "c5c971c0-ba8e-4038-adab-99625f5cdfb8",
              "type": "identities"
            },
            {
              "id": "c36dabf5-4606-4605-83f2-a5d9a8a3055b",
              "type": "identities"
            },
            {
              "id": "dd48c8f9-87e4-4416-839b-2011478f3ea3",
              "type": "identities"
            },
            {
              "id": "1e04a595-b148-4a91-ab5e-a216869a9425",
              "type": "identities"
            },
            {
              "id": "23e52bdc-fb20-482d-b2e1-f82c51691878",
              "type": "identities"
            },
            {
              "id": "243e9c85-a2a4-4fe2-88f3-7ffd331e73f6",
              "type": "identities"
            },
            {
              "id": "b1836eaf-3317-4a25-93fe-2eb91551f741",
              "type": "identities"
            },
            {
              "id": "a4b0ac33-3835-401a-9ad1-2897d00b484e",
              "type": "identities"
            },
            {
              "id": "13608380-02d7-4293-b2d2-3c5442633209",
              "type": "identities"
            },
            {
              "id": "08556c9d-e1a9-4edb-93e2-436e6452bdb8",
              "type": "identities"
            },
            {
              "id": "be864f44-d7fc-40c2-b2bc-1014209d8a2c",
              "type": "identities"
            },
            {
              "id": "cad8995c-5f1c-4f04-803b-b8325821ac1c",
              "type": "identities"
            }
          ]
        },
        "comments": {
          "data": []
        },
        "groups": {
          "data": [
            {
              "id": "1d7ded8e-6823-4cf6-a652-01791a9899e0",
              "type": "groups"
            }
          ]
        },
        "images": {
          "data": []
        },
        "documents": {
          "data": []
        },
        "touchpoints": {
          "data": [
            {
              "id": "c301ba82-11a7-40f7-98da-73d880b027d0",
              "type": "touchpoints"
            },
            {
              "id": "64d542a5-eeac-451d-9101-2d38716d556e",
              "type": "touchpoints"
            },
            {
              "id": "7c5b22f6-a939-4069-b409-96bfd0fde96a",
              "type": "touchpoints"
            },
            {
              "id": "ff8e7381-d78a-45d1-aaf4-015e46dc94e4",
              "type": "touchpoints"
            },
            {
              "id": "a6ef2680-16a7-4215-b6db-0d6b3e26a1e9",
              "type": "touchpoints"
            },
            {
              "id": "db1675e7-18cb-451d-aa3f-f5cb4b217396",
              "type": "touchpoints"
            },
            {
              "id": "ab4d37ae-9ca0-4e27-9297-747cea40dc31",
              "type": "touchpoints"
            },
            {
              "id": "7f125fcc-544c-4f89-970d-d780fd384d37",
              "type": "touchpoints"
            },
            {
              "id": "880b8ae2-752b-431c-bae3-8c06c2d67f7d",
              "type": "touchpoints"
            },
            {
              "id": "50206a41-18a7-4b28-abf2-5af1e9f637b9",
              "type": "touchpoints"
            },
            {
              "id": "2cec1e92-0688-4dd3-9cbe-88e41bc6ba76",
              "type": "touchpoints"
            },
            {
              "id": "711952de-6f78-426b-a969-c26ae79b111d",
              "type": "touchpoints"
            },
            {
              "id": "1bf7b58b-bb25-4cd4-873a-23219eabded3",
              "type": "touchpoints"
            },
            {
              "id": "79cfa409-3dcb-41cf-b612-bb6b5b25185b",
              "type": "touchpoints"
            },
            {
              "id": "ea2f6087-de75-4c16-a031-7034ec5f8ba1",
              "type": "touchpoints"
            },
            {
              "id": "70ffa21f-e6cc-487f-b5ee-b4b4c81b698c",
              "type": "touchpoints"
            },
            {
              "id": "9e6b8c56-f2d9-4410-b4e4-7a1c8ffcd835",
              "type": "touchpoints"
            },
            {
              "id": "668513ea-8e87-47ea-935a-99331a8e318a",
              "type": "touchpoints"
            },
            {
              "id": "5073a5fb-3431-4a67-a936-7ffffd97751b",
              "type": "touchpoints"
            },
            {
              "id": "3d9f2700-72af-4b02-8d83-6c9b37df2ddd",
              "type": "touchpoints"
            },
            {
              "id": "3de805ef-95de-4fbf-ad8e-25f5e1041f44",
              "type": "touchpoints"
            },
            {
              "id": "369bcaf5-644d-44d7-aa7f-07435bac70ee",
              "type": "touchpoints"
            },
            {
              "id": "f63eef4b-a357-4845-b45e-470748f4ff78",
              "type": "touchpoints"
            },
            {
              "id": "6e4173ea-ff5d-46ee-bfb4-8e503001d9a7",
              "type": "touchpoints"
            },
            {
              "id": "3d4001a1-e7e4-42e0-a8cf-0a3222af7a45",
              "type": "touchpoints"
            },
            {
              "id": "4652bc58-69cf-43ca-ab7a-e3fc5808a0c4",
              "type": "touchpoints"
            },
            {
              "id": "1368c56c-594c-4d6c-a15f-15bb2f9346b5",
              "type": "touchpoints"
            },
            {
              "id": "4d918775-60e7-4352-b5d3-77c748cc32bb",
              "type": "touchpoints"
            },
            {
              "id": "1b405c07-88e1-4553-b508-a5524d68fbbd",
              "type": "touchpoints"
            },
            {
              "id": "197a0a5b-f785-445e-9f48-2606fecd2ee6",
              "type": "touchpoints"
            },
            {
              "id": "1ae53d0c-ef1f-467c-9b65-7d348dc4fa05",
              "type": "touchpoints"
            },
            {
              "id": "dbed4545-b663-4003-a9f6-ca44c084a250",
              "type": "touchpoints"
            },
            {
              "id": "4071af97-6f1f-4e6b-b040-fec00ebacaf3",
              "type": "touchpoints"
            },
            {
              "id": "9237a936-5b02-4f32-9799-0960cd5ac58a",
              "type": "touchpoints"
            },
            {
              "id": "9b5f0056-fcfc-410f-bc88-74f775a087ec",
              "type": "touchpoints"
            },
            {
              "id": "1e1bcc57-1ab2-4b2c-acb0-2766b8ef6603",
              "type": "touchpoints"
            },
            {
              "id": "aee7376f-c3b7-4283-af96-e6be9d93c62c",
              "type": "touchpoints"
            },
            {
              "id": "9a824289-29be-43ce-abb8-3ca73ccb4c8f",
              "type": "touchpoints"
            },
            {
              "id": "14dbf152-2281-4898-986c-5744395f9efd",
              "type": "touchpoints"
            },
            {
              "id": "ff2bb763-9189-41dc-a851-09431f2adb4e",
              "type": "touchpoints"
            },
            {
              "id": "12673559-dc4a-47bd-aa02-64347b96a773",
              "type": "touchpoints"
            },
            {
              "id": "2f7fd331-84bf-45e1-bd23-3c312f6a4530",
              "type": "touchpoints"
            },
            {
              "id": "6153f054-2918-484a-aa06-9a7f606437bc",
              "type": "touchpoints"
            },
            {
              "id": "1edb62f8-e9cd-41df-913d-b7edfb047cb7",
              "type": "touchpoints"
            },
            {
              "id": "9c76dc10-6421-4b04-b519-813eaa171429",
              "type": "touchpoints"
            },
            {
              "id": "a3c2cc88-8592-4a40-a406-1cd1d953a92a",
              "type": "touchpoints"
            },
            {
              "id": "906f2e59-1dca-4c68-8457-ff467a9f03b1",
              "type": "touchpoints"
            },
            {
              "id": "ccc348f6-9ed7-499f-a6d7-87911a2b53b8",
              "type": "touchpoints"
            },
            {
              "id": "2fe4ced2-9298-4679-a781-8eadd2e8deb9",
              "type": "touchpoints"
            },
            {
              "id": "64c2b30d-6cfb-4e54-a77f-0c7b7a6780c0",
              "type": "touchpoints"
            },
            {
              "id": "1ee76913-7760-4407-be72-8f331ea74fe9",
              "type": "touchpoints"
            },
            {
              "id": "70f8d96c-c82b-47e3-b768-dd997df9def2",
              "type": "touchpoints"
            },
            {
              "id": "edd1b66c-9c37-4036-8729-09cd89e2ebc3",
              "type": "touchpoints"
            },
            {
              "id": "0e7dec4f-4e3d-4945-adf4-c13beb58e708",
              "type": "touchpoints"
            },
            {
              "id": "c1d693e4-afab-463f-bdbe-9c2ff32d49af",
              "type": "touchpoints"
            },
            {
              "id": "020e82e4-83ee-493f-af45-8c7f3bf6a63c",
              "type": "touchpoints"
            },
            {
              "id": "4d70e3b5-fcff-414d-aeed-46f922df3f76",
              "type": "touchpoints"
            },
            {
              "id": "6a27cf7e-7efd-457a-9bdf-7f3feb72ef5e",
              "type": "touchpoints"
            }
          ]
        },
        "roles": {
          "data": [
            {
              "id": "74b8d086-3a73-4ce3-b0ec-528b6fe348c0",
              "type": "roles"
            },
            {
              "id": "a3f41f64-a5e6-4db2-81b2-b9d5285ee9eb",
              "type": "roles"
            },
            {
              "id": "b44a48b8-131f-49ae-8152-8f389b2107f9",
              "type": "roles"
            },
            {
              "id": "b07456d2-4ec3-4aad-be83-26f4da23d95f",
              "type": "roles"
            },
            {
              "id": "4dce7276-82e9-4dab-bbcd-4166e13ad202",
              "type": "roles"
            },
            {
              "id": "c8881052-3ec6-4197-bce5-827a1ffa2a5e",
              "type": "roles"
            },
            {
              "id": "b6698f9c-d58d-4509-b11d-417444a56d61",
              "type": "roles"
            },
            {
              "id": "4d70f55a-533c-46c9-bcfa-27075b66a550",
              "type": "roles"
            },
            {
              "id": "4246d7eb-58a9-4a78-87a9-b57a59dd8412",
              "type": "roles"
            },
            {
              "id": "c977f367-49e5-487a-a57a-33026022d284",
              "type": "roles"
            },
            {
              "id": "430b29b3-9417-4bf2-a96a-d754207b94d9",
              "type": "roles"
            },
            {
              "id": "3b44fe40-88c3-4742-b64d-abc724ecf7c6",
              "type": "roles"
            },
            {
              "id": "c678f9cd-4d7f-4514-8b83-ce9ce7022744",
              "type": "roles"
            },
            {
              "id": "728cfeb2-8742-4620-b7a9-954eb6545b72",
              "type": "roles"
            },
            {
              "id": "6384464e-accb-461e-acd9-671d5cf6b7e9",
              "type": "roles"
            },
            {
              "id": "ab6dbcda-8038-471b-9b05-f538e4e39f3b",
              "type": "roles"
            },
            {
              "id": "f0a0bbd5-f126-4c26-9e98-160436f52d9d",
              "type": "roles"
            }
          ]
        },
        "received_messages": {
          "data": [
            {
              "id": "d948568f-0386-4fb0-af94-5b68ad2688b9",
              "type": "messages"
            }
          ]
        },
        "sent_messages": {
          "data": []
        },
        "leaves": {
          "data": []
        }
      }
    },
    {
      "id": "b79c135e-4eb6-4e65-9765-672369c47721",
      "type": "addresses",
      "attributes": {
        "uuid": "b79c135e-4eb6-4e65-9765-672369c47721",
        "type": "work",
        "company_name": null,
        "city": "montréal",
        "zip_code": "h2m 1v5",
        "address1": "8806 8806 foucher",
        "address2": "",
        "state_name": "QC",
        "country_code": "CA",
        "created_at": "2016-08-04T23:19:50.446Z",
        "updated_at": "2016-08-04T23:19:50.446Z",
        "deleted_at": null,
        "active": true,
        "primary": true,
        "country_name": "Canada"
      },
      "relationships": {
        "addressable": {
          "data": {
            "id": "6fd574b1-4772-45ad-a238-1ee466f312ac",
            "type": "people"
          }
        },
        "organization": {
          "data": null
        },
        "cloned_from": {
          "data": null,
          "meta": {
            "has_same_address_fields": false
          }
        }
      }
    },
    {
      "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
      "type": "intervals",
      "attributes": {
        "uuid": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
        "name": "CPA Annual Membership 2016",
        "name_en": "CPA Annual Membership 2016",
        "name_fr": "ACP Adhésion Annuelle 2016",
        "name_es": "CPA Annual Membership 2016",
        "alternate_name": "CPA Annual Membership 2016",
        "alternate_name_en": "CPA Annual Membership 2016",
        "alternate_name_fr": "ACP Adhésion Annuelle 2016",
        "description": "Annual Membership in the Canadian Physiotherapy Association (CPA)",
        "description_en": "Annual Membership in the Canadian Physiotherapy Association (CPA)",
        "description_fr": "ACP Adhésion Annuelle 2016",
        "description_es": "Annual Membership in the Canadian Physiotherapy Association (CPA)",
        "starts_at": "2016-10-01T07:00:01.000Z",
        "ends_at": "2017-10-01T07:00:00.000Z",
        "deleted_at": null,
        "created_at": "2016-08-04T22:24:05.551Z",
        "updated_at": "2016-08-04T22:24:05.560Z",
        "current": true,
        "available": true,
        "data": {},
        "previous_id": 4,
        "eligible_previous_seasons": [],
        "slug": "cpa-annual-membership-2016",
        "is_root": true
      },
      "relationships": {
        "organization": {
          "data": {
            "id": "c1519a7d-6abc-42e1-bc9b-1f6d1f586e6f",
            "type": "organizations"
          }
        },
        "previous": {
          "data": {
            "id": "580e479f-c374-4fb7-bd0d-a63fe0751258",
            "type": "intervals"
          }
        }
      }
    },
    {
      "id": "ab5445e3-5010-44c3-9b0c-83dcafb80d66",
      "type": "addresses",
      "attributes": {
        "uuid": "ab5445e3-5010-44c3-9b0c-83dcafb80d66",
        "type": "work",
        "company_name": null,
        "city": "montréal",
        "zip_code": "h2m 1v5",
        "address1": "8806 8806 foucher",
        "address2": "",
        "state_name": "QC",
        "country_code": "CA",
        "created_at": "2016-10-18T15:34:32.744Z",
        "updated_at": "2016-10-18T15:34:32.744Z",
        "deleted_at": null,
        "active": true,
        "primary": true,
        "country_name": "Canada"
      },
      "relationships": {
        "addressable": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        },
        "organization": {
          "data": null
        },
        "cloned_from": {
          "data": {
            "id": "b79c135e-4eb6-4e65-9765-672369c47721",
            "type": "addresses"
          },
          "meta": {
            "has_same_address_fields": true
          }
        }
      }
    },
    {
      "id": "4ee057c2-4a32-4b35-8ea9-2454302d656f",
      "type": "payment_options",
      "attributes": {
        "name": "Pay in Full",
        "name_en": "Pay in Full",
        "name_fr": "Payer la somme totale",
        "name_es": "Payer la somme totale",
        "alternate_name": null,
        "alternate_name_en": null,
        "alternate_name_fr": null,
        "alternate_name_es": null,
        "description": null,
        "description_en": null,
        "description_fr": null,
        "description_es": null,
        "updated_at": "2016-08-04T22:24:34.545Z",
        "created_at": "2016-08-04T22:24:34.545Z",
        "deleted_at": null,
        "default": true,
        "payments": 1,
        "weight": 1,
        "slug": "pay-in-full"
      },
      "relationships": {
        "organization": {
          "data": {
            "id": "c1519a7d-6abc-42e1-bc9b-1f6d1f586e6f",
            "type": "organizations"
          }
        },
        "payment_methods": {
          "data": [
            {
              "id": "b8bcce0b-5155-4c19-a36c-a1d7fdabbea9",
              "type": "payment_methods"
            },
            {
              "id": "8d35ae76-115a-4660-9047-375b2dc673f7",
              "type": "payment_methods"
            }
          ]
        }
      }
    },
    {
      "id": "087e15b6-83aa-4ab8-92e8-17f4985d1104",
      "type": "payment_options",
      "attributes": {
        "name": "Monthly Payments",
        "name_en": "Monthly Payments",
        "name_fr": "Paiements mensuels",
        "name_es": "Paiements mensuels",
        "alternate_name": null,
        "alternate_name_en": null,
        "alternate_name_fr": null,
        "alternate_name_es": null,
        "description": null,
        "description_en": null,
        "description_fr": null,
        "description_es": null,
        "updated_at": "2016-08-04T22:24:34.551Z",
        "created_at": "2016-08-04T22:24:34.551Z",
        "deleted_at": null,
        "default": false,
        "payments": 12,
        "weight": 2,
        "slug": "monthly-payments"
      },
      "relationships": {
        "organization": {
          "data": {
            "id": "c1519a7d-6abc-42e1-bc9b-1f6d1f586e6f",
            "type": "organizations"
          }
        },
        "payment_methods": {
          "data": [
            {
              "id": "b8bcce0b-5155-4c19-a36c-a1d7fdabbea9",
              "type": "payment_methods"
            }
          ]
        }
      }
    },
    {
      "id": "802fc626-756d-48e7-9b7f-d0355f5ad1b3",
      "type": "line_items",
      "attributes": {
        "uuid": "802fc626-756d-48e7-9b7f-d0355f5ad1b3",
        "quantity": 1,
        "price": "0.0",
        "currency": "cad",
        "amount": "0.0",
        "total": "0.0",
        "subtotal": "0.0",
        "tax_total": "0.0",
        "adjustment_total": "0.0",
        "manual_adjustment_total": "0.0",
        "promotion_total": "0.0",
        "interval_total": "0.0",
        "leave_total": "0.0",
        "additional_tax_total": "0.0",
        "included_tax_total": "0.0",
        "updated_at": "2016-10-18T15:34:56.819Z",
        "created_at": "2016-10-18T15:34:33.058Z",
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true,
        "refunded": null
      },
      "relationships": {
        "adjustments": {
          "data": []
        },
        "variant": {
          "data": {
            "id": "9b2beef0-066a-4d95-b7dd-92bcdeae85cb",
            "type": "variants"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "9b2beef0-066a-4d95-b7dd-92bcdeae85cb",
      "type": "variants",
      "attributes": {
        "uuid": "9b2beef0-066a-4d95-b7dd-92bcdeae85cb",
        "price": "0.0",
        "line_item_name": "MEMBERSHIP Entry-level Student",
        "line_item_name_en": "MEMBERSHIP Entry-level Student",
        "line_item_name_fr": "ADHÉSION ",
        "line_item_name_es": "TRANSLATION MISSING: ES.MEMBERSHIP ",
        "type": "VariantMembership",
        "name": "Entry-level Student",
        "name_en": "Entry-level Student",
        "name_fr": null,
        "name_es": null,
        "description": "Physiotherapy students who do not yet have a License #",
        "description_en": "Physiotherapy students who do not yet have a License #",
        "description_fr": "Physiotherapy students who do not yet have a License #",
        "description_es": "Physiotherapy students who do not yet have a License #",
        "orderable_type_name_en": "Membership",
        "orderable_type_name_fr": "Adhésion",
        "orderable_type_name_es": "translation missing: es.membership",
        "currency": "cad",
        "created_at": "2016-08-04T22:24:06.899Z",
        "updated_at": "2016-08-04T22:24:06.899Z",
        "deleted_at": null,
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true
      },
      "relationships": {
        "interval": {
          "data": {
            "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
            "type": "intervals"
          }
        },
        "orderable": {
          "data": {
            "id": "db02f405-8b40-47c4-b389-fcb836e0f8b3",
            "type": "memberships"
          }
        }
      }
    },
    {
      "id": "3c0ad488-ef1c-471e-beb2-ccd4045da6f6",
      "type": "line_items",
      "attributes": {
        "uuid": "3c0ad488-ef1c-471e-beb2-ccd4045da6f6",
        "quantity": 1,
        "price": "35.0",
        "currency": "cad",
        "amount": "35.0",
        "total": "0.0",
        "subtotal": "0.0",
        "tax_total": "0.0",
        "adjustment_total": "-35.0",
        "manual_adjustment_total": "0.0",
        "promotion_total": "-35.0",
        "interval_total": "0.0",
        "leave_total": "0.0",
        "additional_tax_total": "0.0",
        "included_tax_total": "0.0",
        "updated_at": "2016-10-18T15:34:57.806Z",
        "created_at": "2016-10-18T15:34:33.213Z",
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true,
        "refunded": null
      },
      "relationships": {
        "adjustments": {
          "data": [
            {
              "id": "1ee43ad6-6641-414b-95b3-73307b1be1bb",
              "type": "adjustments"
            }
          ]
        },
        "variant": {
          "data": {
            "id": "228ad6cc-3db7-4b98-87a9-4b21567d0a36",
            "type": "variants"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "1ee43ad6-6641-414b-95b3-73307b1be1bb",
      "type": "adjustments",
      "attributes": {
        "amount": "-35.0",
        "label": "Student Division Discount",
        "label_en": "Student Division Discount",
        "label_fr": "Student Division Discount",
        "label_es": "Student Division Discount",
        "eligible": true,
        "state": "active",
        "created_at": "2016-10-18T15:34:57.792Z",
        "updated_at": "2016-10-18T15:34:57.792Z",
        "type": "money",
        "percentage": "0.0",
        "source_type": "promotion"
      },
      "relationships": {
        "adjustable": {
          "data": {
            "id": "3c0ad488-ef1c-471e-beb2-ccd4045da6f6",
            "type": "line_items"
          }
        },
        "source": {
          "data": {
            "id": "475cfd6f-861c-425b-92d6-080fa5c935cf",
            "type": "promotions"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "228ad6cc-3db7-4b98-87a9-4b21567d0a36",
      "type": "variants",
      "attributes": {
        "uuid": "228ad6cc-3db7-4b98-87a9-4b21567d0a36",
        "price": "35.0",
        "line_item_name": "MEMBERSHIP Acupuncture",
        "line_item_name_en": "MEMBERSHIP Acupuncture",
        "line_item_name_fr": "ADHÉSION Acupuncture",
        "line_item_name_es": "TRANSLATION MISSING: ES.MEMBERSHIP ",
        "type": "VariantMembership",
        "name": "Acupuncture",
        "name_en": "Acupuncture",
        "name_fr": "Acupuncture",
        "name_es": null,
        "description": "Acupuncture Division",
        "description_en": "Acupuncture Division",
        "description_fr": "Acupuncture Division",
        "description_es": "Acupuncture Division",
        "orderable_type_name_en": "Membership",
        "orderable_type_name_fr": "Adhésion",
        "orderable_type_name_es": "translation missing: es.membership",
        "currency": "cad",
        "created_at": "2016-08-04T22:24:32.104Z",
        "updated_at": "2016-08-04T22:24:32.104Z",
        "deleted_at": null,
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true
      },
      "relationships": {
        "interval": {
          "data": {
            "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
            "type": "intervals"
          }
        },
        "orderable": {
          "data": {
            "id": "eea4bed7-3f05-477a-86d1-6c1255cb6bc7",
            "type": "memberships"
          }
        }
      }
    },
    {
      "id": "04aa2762-a00c-46af-b1c5-627e13019a68",
      "type": "line_items",
      "attributes": {
        "uuid": "04aa2762-a00c-46af-b1c5-627e13019a68",
        "quantity": 1,
        "price": "30.0",
        "currency": "cad",
        "amount": "30.0",
        "total": "0.0",
        "subtotal": "0.0",
        "tax_total": "0.0",
        "adjustment_total": "-30.0",
        "manual_adjustment_total": "0.0",
        "promotion_total": "-30.0",
        "interval_total": "0.0",
        "leave_total": "0.0",
        "additional_tax_total": "0.0",
        "included_tax_total": "0.0",
        "updated_at": "2016-10-18T15:34:57.986Z",
        "created_at": "2016-10-18T15:34:33.271Z",
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true,
        "refunded": null
      },
      "relationships": {
        "adjustments": {
          "data": [
            {
              "id": "c620c814-5e25-46b0-bbf8-f043e25b07b2",
              "type": "adjustments"
            }
          ]
        },
        "variant": {
          "data": {
            "id": "8be53cac-2b71-4c1a-a6bd-2c82dd2d7222",
            "type": "variants"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "c620c814-5e25-46b0-bbf8-f043e25b07b2",
      "type": "adjustments",
      "attributes": {
        "amount": "-30.0",
        "label": "Student Division Discount",
        "label_en": "Student Division Discount",
        "label_fr": "Student Division Discount",
        "label_es": "Student Division Discount",
        "eligible": true,
        "state": "active",
        "created_at": "2016-10-18T15:34:57.972Z",
        "updated_at": "2016-10-18T15:34:57.972Z",
        "type": "money",
        "percentage": "0.0",
        "source_type": "promotion"
      },
      "relationships": {
        "adjustable": {
          "data": {
            "id": "04aa2762-a00c-46af-b1c5-627e13019a68",
            "type": "line_items"
          }
        },
        "source": {
          "data": {
            "id": "475cfd6f-861c-425b-92d6-080fa5c935cf",
            "type": "promotions"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "8be53cac-2b71-4c1a-a6bd-2c82dd2d7222",
      "type": "variants",
      "attributes": {
        "uuid": "8be53cac-2b71-4c1a-a6bd-2c82dd2d7222",
        "price": "30.0",
        "line_item_name": "MEMBERSHIP Cardiorespiratory",
        "line_item_name_en": "MEMBERSHIP Cardiorespiratory",
        "line_item_name_fr": "ADHÉSION Cardiorespiratoire",
        "line_item_name_es": "TRANSLATION MISSING: ES.MEMBERSHIP ",
        "type": "VariantMembership",
        "name": "Cardiorespiratory",
        "name_en": "Cardiorespiratory",
        "name_fr": "Cardiorespiratoire",
        "name_es": null,
        "description": "Cardiorespiratory Division",
        "description_en": "Cardiorespiratory Division",
        "description_fr": "Cardiorespiratory Division",
        "description_es": "Cardiorespiratory Division",
        "orderable_type_name_en": "Membership",
        "orderable_type_name_fr": "Adhésion",
        "orderable_type_name_es": "translation missing: es.membership",
        "currency": "cad",
        "created_at": "2016-08-04T22:24:32.325Z",
        "updated_at": "2016-08-04T22:24:32.325Z",
        "deleted_at": null,
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true
      },
      "relationships": {
        "interval": {
          "data": {
            "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
            "type": "intervals"
          }
        },
        "orderable": {
          "data": {
            "id": "5bfd2125-debf-442e-bac6-4860b6a700d0",
            "type": "memberships"
          }
        }
      }
    },
    {
      "id": "f1d53497-9ce8-42a0-a9ad-8572a79e09c8",
      "type": "line_items",
      "attributes": {
        "uuid": "f1d53497-9ce8-42a0-a9ad-8572a79e09c8",
        "quantity": 1,
        "price": "30.0",
        "currency": "cad",
        "amount": "30.0",
        "total": "0.0",
        "subtotal": "0.0",
        "tax_total": "0.0",
        "adjustment_total": "-30.0",
        "manual_adjustment_total": "0.0",
        "promotion_total": "-30.0",
        "interval_total": "0.0",
        "leave_total": "0.0",
        "additional_tax_total": "0.0",
        "included_tax_total": "0.0",
        "updated_at": "2016-10-18T15:34:58.159Z",
        "created_at": "2016-10-18T15:34:33.329Z",
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true,
        "refunded": null
      },
      "relationships": {
        "adjustments": {
          "data": [
            {
              "id": "1626443b-f685-47d7-89db-dbfb18a950cd",
              "type": "adjustments"
            }
          ]
        },
        "variant": {
          "data": {
            "id": "838b86ed-520e-4e25-889c-638900ca817e",
            "type": "variants"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "1626443b-f685-47d7-89db-dbfb18a950cd",
      "type": "adjustments",
      "attributes": {
        "amount": "-30.0",
        "label": "Student Division Discount",
        "label_en": "Student Division Discount",
        "label_fr": "Student Division Discount",
        "label_es": "Student Division Discount",
        "eligible": true,
        "state": "active",
        "created_at": "2016-10-18T15:34:58.145Z",
        "updated_at": "2016-10-18T15:34:58.145Z",
        "type": "money",
        "percentage": "0.0",
        "source_type": "promotion"
      },
      "relationships": {
        "adjustable": {
          "data": {
            "id": "f1d53497-9ce8-42a0-a9ad-8572a79e09c8",
            "type": "line_items"
          }
        },
        "source": {
          "data": {
            "id": "475cfd6f-861c-425b-92d6-080fa5c935cf",
            "type": "promotions"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "838b86ed-520e-4e25-889c-638900ca817e",
      "type": "variants",
      "attributes": {
        "uuid": "838b86ed-520e-4e25-889c-638900ca817e",
        "price": "30.0",
        "line_item_name": "MEMBERSHIP Oncology",
        "line_item_name_en": "MEMBERSHIP Oncology",
        "line_item_name_fr": "ADHÉSION Oncologie",
        "line_item_name_es": "TRANSLATION MISSING: ES.MEMBERSHIP ",
        "type": "VariantMembership",
        "name": "Oncology",
        "name_en": "Oncology",
        "name_fr": "Oncologie",
        "name_es": null,
        "description": "Oncology Division",
        "description_en": "Oncology Division",
        "description_fr": "Oncology Division",
        "description_es": "Oncology Division",
        "orderable_type_name_en": "Membership",
        "orderable_type_name_fr": "Adhésion",
        "orderable_type_name_es": "translation missing: es.membership",
        "currency": "cad",
        "created_at": "2016-08-04T22:24:32.767Z",
        "updated_at": "2016-08-04T22:24:32.767Z",
        "deleted_at": null,
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true
      },
      "relationships": {
        "interval": {
          "data": {
            "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
            "type": "intervals"
          }
        },
        "orderable": {
          "data": {
            "id": "17e799e0-5385-4d37-a727-b95143c11030",
            "type": "memberships"
          }
        }
      }
    },
    {
      "id": "0f5d0989-d8f5-42c4-94ea-a08258640f07",
      "type": "line_items",
      "attributes": {
        "uuid": "0f5d0989-d8f5-42c4-94ea-a08258640f07",
        "quantity": 1,
        "price": "40.0",
        "currency": "cad",
        "amount": "40.0",
        "total": "0.0",
        "subtotal": "0.0",
        "tax_total": "0.0",
        "adjustment_total": "-40.0",
        "manual_adjustment_total": "0.0",
        "promotion_total": "-40.0",
        "interval_total": "0.0",
        "leave_total": "0.0",
        "additional_tax_total": "0.0",
        "included_tax_total": "0.0",
        "updated_at": "2016-10-18T15:34:58.332Z",
        "created_at": "2016-10-18T15:34:33.403Z",
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true,
        "refunded": null
      },
      "relationships": {
        "adjustments": {
          "data": [
            {
              "id": "a73e96ed-c39c-48ee-9cbf-3f56bb6f7376",
              "type": "adjustments"
            }
          ]
        },
        "variant": {
          "data": {
            "id": "ff4e3d64-dbcb-4baf-8687-21bb671a219c",
            "type": "variants"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "a73e96ed-c39c-48ee-9cbf-3f56bb6f7376",
      "type": "adjustments",
      "attributes": {
        "amount": "-40.0",
        "label": "Student Division Discount",
        "label_en": "Student Division Discount",
        "label_fr": "Student Division Discount",
        "label_es": "Student Division Discount",
        "eligible": true,
        "state": "active",
        "created_at": "2016-10-18T15:34:58.318Z",
        "updated_at": "2016-10-18T15:34:58.318Z",
        "type": "money",
        "percentage": "0.0",
        "source_type": "promotion"
      },
      "relationships": {
        "adjustable": {
          "data": {
            "id": "0f5d0989-d8f5-42c4-94ea-a08258640f07",
            "type": "line_items"
          }
        },
        "source": {
          "data": {
            "id": "475cfd6f-861c-425b-92d6-080fa5c935cf",
            "type": "promotions"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "ff4e3d64-dbcb-4baf-8687-21bb671a219c",
      "type": "variants",
      "attributes": {
        "uuid": "ff4e3d64-dbcb-4baf-8687-21bb671a219c",
        "price": "40.0",
        "line_item_name": "MEMBERSHIP Leadership",
        "line_item_name_en": "MEMBERSHIP Leadership",
        "line_item_name_fr": "ADHÉSION Leadership",
        "line_item_name_es": "TRANSLATION MISSING: ES.MEMBERSHIP ",
        "type": "VariantMembership",
        "name": "Leadership",
        "name_en": "Leadership",
        "name_fr": "Leadership",
        "name_es": null,
        "description": "Leadership Division",
        "description_en": "Leadership Division",
        "description_fr": "Leadership Division",
        "description_es": "Leadership Division",
        "orderable_type_name_en": "Membership",
        "orderable_type_name_fr": "Adhésion",
        "orderable_type_name_es": "translation missing: es.membership",
        "currency": "cad",
        "created_at": "2016-08-04T22:24:32.549Z",
        "updated_at": "2016-08-04T22:24:32.549Z",
        "deleted_at": null,
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true
      },
      "relationships": {
        "interval": {
          "data": {
            "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
            "type": "intervals"
          }
        },
        "orderable": {
          "data": {
            "id": "0a278357-6d5a-40dc-8e74-cbe1679c237b",
            "type": "memberships"
          }
        }
      }
    },
    {
      "id": "21d48987-7a66-4f8e-97f7-f043ceca63ad",
      "type": "line_items",
      "attributes": {
        "uuid": "21d48987-7a66-4f8e-97f7-f043ceca63ad",
        "quantity": 1,
        "price": "55.0",
        "currency": "cad",
        "amount": "55.0",
        "total": "0.0",
        "subtotal": "0.0",
        "tax_total": "0.0",
        "adjustment_total": "-55.0",
        "manual_adjustment_total": "0.0",
        "promotion_total": "-55.0",
        "interval_total": "0.0",
        "leave_total": "0.0",
        "additional_tax_total": "0.0",
        "included_tax_total": "0.0",
        "updated_at": "2016-10-18T15:34:58.505Z",
        "created_at": "2016-10-18T15:34:33.458Z",
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true,
        "refunded": null
      },
      "relationships": {
        "adjustments": {
          "data": [
            {
              "id": "b17f08c1-8f8f-46f4-9cb1-9737656da797",
              "type": "adjustments"
            }
          ]
        },
        "variant": {
          "data": {
            "id": "60156659-e4aa-43ec-acfa-4e8e61be604d",
            "type": "variants"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "b17f08c1-8f8f-46f4-9cb1-9737656da797",
      "type": "adjustments",
      "attributes": {
        "amount": "-55.0",
        "label": "Student Division Discount",
        "label_en": "Student Division Discount",
        "label_fr": "Student Division Discount",
        "label_es": "Student Division Discount",
        "eligible": true,
        "state": "active",
        "created_at": "2016-10-18T15:34:58.491Z",
        "updated_at": "2016-10-18T15:34:58.491Z",
        "type": "money",
        "percentage": "0.0",
        "source_type": "promotion"
      },
      "relationships": {
        "adjustable": {
          "data": {
            "id": "21d48987-7a66-4f8e-97f7-f043ceca63ad",
            "type": "line_items"
          }
        },
        "source": {
          "data": {
            "id": "475cfd6f-861c-425b-92d6-080fa5c935cf",
            "type": "promotions"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "60156659-e4aa-43ec-acfa-4e8e61be604d",
      "type": "variants",
      "attributes": {
        "uuid": "60156659-e4aa-43ec-acfa-4e8e61be604d",
        "price": "55.0",
        "line_item_name": "MEMBERSHIP Orthopaedics",
        "line_item_name_en": "MEMBERSHIP Orthopaedics",
        "line_item_name_fr": "ADHÉSION Orthopédie",
        "line_item_name_es": "TRANSLATION MISSING: ES.MEMBERSHIP ",
        "type": "VariantMembership",
        "name": "Orthopaedics",
        "name_en": "Orthopaedics",
        "name_fr": "Orthopédie",
        "name_es": null,
        "description": "Orthopaedics Division",
        "description_en": "Orthopaedics Division",
        "description_fr": "Orthopaedics Division",
        "description_es": "Orthopaedics Division",
        "orderable_type_name_en": "Membership",
        "orderable_type_name_fr": "Adhésion",
        "orderable_type_name_es": "translation missing: es.membership",
        "currency": "cad",
        "created_at": "2016-08-04T22:24:32.875Z",
        "updated_at": "2016-08-04T22:24:32.875Z",
        "deleted_at": null,
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true
      },
      "relationships": {
        "interval": {
          "data": {
            "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
            "type": "intervals"
          }
        },
        "orderable": {
          "data": {
            "id": "ea61dc5a-6086-4b84-a964-378ba31c59a3",
            "type": "memberships"
          }
        }
      }
    },
    {
      "id": "4d5eb8b6-5f23-4dbe-b087-b8f0dc7f147c",
      "type": "line_items",
      "attributes": {
        "uuid": "4d5eb8b6-5f23-4dbe-b087-b8f0dc7f147c",
        "quantity": 1,
        "price": "30.0",
        "currency": "cad",
        "amount": "30.0",
        "total": "0.0",
        "subtotal": "0.0",
        "tax_total": "0.0",
        "adjustment_total": "-30.0",
        "manual_adjustment_total": "0.0",
        "promotion_total": "-30.0",
        "interval_total": "0.0",
        "leave_total": "0.0",
        "additional_tax_total": "0.0",
        "included_tax_total": "0.0",
        "updated_at": "2016-10-18T15:34:58.693Z",
        "created_at": "2016-10-18T15:34:33.512Z",
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true,
        "refunded": null
      },
      "relationships": {
        "adjustments": {
          "data": [
            {
              "id": "2e66023e-7217-44ce-9d3f-7e150d039235",
              "type": "adjustments"
            }
          ]
        },
        "variant": {
          "data": {
            "id": "676d477d-dcee-4a1c-be0c-4b45cf99fa77",
            "type": "variants"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "2e66023e-7217-44ce-9d3f-7e150d039235",
      "type": "adjustments",
      "attributes": {
        "amount": "-30.0",
        "label": "Student Division Discount",
        "label_en": "Student Division Discount",
        "label_fr": "Student Division Discount",
        "label_es": "Student Division Discount",
        "eligible": true,
        "state": "active",
        "created_at": "2016-10-18T15:34:58.680Z",
        "updated_at": "2016-10-18T15:34:58.680Z",
        "type": "money",
        "percentage": "0.0",
        "source_type": "promotion"
      },
      "relationships": {
        "adjustable": {
          "data": {
            "id": "4d5eb8b6-5f23-4dbe-b087-b8f0dc7f147c",
            "type": "line_items"
          }
        },
        "source": {
          "data": {
            "id": "475cfd6f-861c-425b-92d6-080fa5c935cf",
            "type": "promotions"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "676d477d-dcee-4a1c-be0c-4b45cf99fa77",
      "type": "variants",
      "attributes": {
        "uuid": "676d477d-dcee-4a1c-be0c-4b45cf99fa77",
        "price": "30.0",
        "line_item_name": "MEMBERSHIP Neurosciences",
        "line_item_name_en": "MEMBERSHIP Neurosciences",
        "line_item_name_fr": "ADHÉSION Neurosciences",
        "line_item_name_es": "TRANSLATION MISSING: ES.MEMBERSHIP ",
        "type": "VariantMembership",
        "name": "Neurosciences",
        "name_en": "Neurosciences",
        "name_fr": "Neurosciences",
        "name_es": null,
        "description": "Neurosciences Division",
        "description_en": "Neurosciences Division",
        "description_fr": "Neurosciences Division",
        "description_es": "Neurosciences Division",
        "orderable_type_name_en": "Membership",
        "orderable_type_name_fr": "Adhésion",
        "orderable_type_name_es": "translation missing: es.membership",
        "currency": "cad",
        "created_at": "2016-08-04T22:24:32.659Z",
        "updated_at": "2016-08-04T22:24:32.659Z",
        "deleted_at": null,
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true
      },
      "relationships": {
        "interval": {
          "data": {
            "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
            "type": "intervals"
          }
        },
        "orderable": {
          "data": {
            "id": "995d3aed-3a30-4989-9198-083d69a9ab2a",
            "type": "memberships"
          }
        }
      }
    },
    {
      "id": "6a2bc618-42f5-428e-8c0a-adf374826637",
      "type": "line_items",
      "attributes": {
        "uuid": "6a2bc618-42f5-428e-8c0a-adf374826637",
        "quantity": 1,
        "price": "35.0",
        "currency": "cad",
        "amount": "35.0",
        "total": "0.0",
        "subtotal": "0.0",
        "tax_total": "0.0",
        "adjustment_total": "-35.0",
        "manual_adjustment_total": "0.0",
        "promotion_total": "-35.0",
        "interval_total": "0.0",
        "leave_total": "0.0",
        "additional_tax_total": "0.0",
        "included_tax_total": "0.0",
        "updated_at": "2016-10-18T15:34:58.865Z",
        "created_at": "2016-10-18T15:34:33.566Z",
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true,
        "refunded": null
      },
      "relationships": {
        "adjustments": {
          "data": [
            {
              "id": "52a05dbf-d551-4c84-8199-b884f8a27ef7",
              "type": "adjustments"
            }
          ]
        },
        "variant": {
          "data": {
            "id": "75245915-8266-4c0e-8e6e-23a4d0cf25a4",
            "type": "variants"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "52a05dbf-d551-4c84-8199-b884f8a27ef7",
      "type": "adjustments",
      "attributes": {
        "amount": "-35.0",
        "label": "Student Division Discount",
        "label_en": "Student Division Discount",
        "label_fr": "Student Division Discount",
        "label_es": "Student Division Discount",
        "eligible": true,
        "state": "active",
        "created_at": "2016-10-18T15:34:58.851Z",
        "updated_at": "2016-10-18T15:34:58.851Z",
        "type": "money",
        "percentage": "0.0",
        "source_type": "promotion"
      },
      "relationships": {
        "adjustable": {
          "data": {
            "id": "6a2bc618-42f5-428e-8c0a-adf374826637",
            "type": "line_items"
          }
        },
        "source": {
          "data": {
            "id": "475cfd6f-861c-425b-92d6-080fa5c935cf",
            "type": "promotions"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "75245915-8266-4c0e-8e6e-23a4d0cf25a4",
      "type": "variants",
      "attributes": {
        "uuid": "75245915-8266-4c0e-8e6e-23a4d0cf25a4",
        "price": "35.0",
        "line_item_name": "MEMBERSHIP Senior's Health",
        "line_item_name_en": "MEMBERSHIP Senior's Health",
        "line_item_name_fr": "ADHÉSION Santé des aînés",
        "line_item_name_es": "TRANSLATION MISSING: ES.MEMBERSHIP ",
        "type": "VariantMembership",
        "name": "Senior's Health",
        "name_en": "Senior's Health",
        "name_fr": "Santé des aînés",
        "name_es": null,
        "description": "Senior's Health Division",
        "description_en": "Senior's Health Division",
        "description_fr": "Senior's Health Division",
        "description_es": "Senior's Health Division",
        "orderable_type_name_en": "Membership",
        "orderable_type_name_fr": "Adhésion",
        "orderable_type_name_es": "translation missing: es.membership",
        "currency": "cad",
        "created_at": "2016-08-04T22:24:33.332Z",
        "updated_at": "2016-08-04T22:24:33.332Z",
        "deleted_at": null,
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true
      },
      "relationships": {
        "interval": {
          "data": {
            "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
            "type": "intervals"
          }
        },
        "orderable": {
          "data": {
            "id": "3e2a6373-c40d-4f1a-93c1-5507d5cb0319",
            "type": "memberships"
          }
        }
      }
    },
    {
      "id": "0dd5ebb0-cddc-4209-9fa5-e174b7180f60",
      "type": "line_items",
      "attributes": {
        "uuid": "0dd5ebb0-cddc-4209-9fa5-e174b7180f60",
        "quantity": 1,
        "price": "55.0",
        "currency": "cad",
        "amount": "55.0",
        "total": "0.0",
        "subtotal": "0.0",
        "tax_total": "0.0",
        "adjustment_total": "-55.0",
        "manual_adjustment_total": "0.0",
        "promotion_total": "-55.0",
        "interval_total": "0.0",
        "leave_total": "0.0",
        "additional_tax_total": "0.0",
        "included_tax_total": "0.0",
        "updated_at": "2016-10-18T15:34:59.033Z",
        "created_at": "2016-10-18T15:34:33.621Z",
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true,
        "refunded": null
      },
      "relationships": {
        "adjustments": {
          "data": [
            {
              "id": "36f7c34c-f637-4354-a87f-4b2cf50408d8",
              "type": "adjustments"
            }
          ]
        },
        "variant": {
          "data": {
            "id": "0c0126de-79cf-4db5-8d2f-875469751755",
            "type": "variants"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "36f7c34c-f637-4354-a87f-4b2cf50408d8",
      "type": "adjustments",
      "attributes": {
        "amount": "-55.0",
        "label": "Student Division Discount",
        "label_en": "Student Division Discount",
        "label_fr": "Student Division Discount",
        "label_es": "Student Division Discount",
        "eligible": true,
        "state": "active",
        "created_at": "2016-10-18T15:34:59.020Z",
        "updated_at": "2016-10-18T15:34:59.020Z",
        "type": "money",
        "percentage": "0.0",
        "source_type": "promotion"
      },
      "relationships": {
        "adjustable": {
          "data": {
            "id": "0dd5ebb0-cddc-4209-9fa5-e174b7180f60",
            "type": "line_items"
          }
        },
        "source": {
          "data": {
            "id": "475cfd6f-861c-425b-92d6-080fa5c935cf",
            "type": "promotions"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "0c0126de-79cf-4db5-8d2f-875469751755",
      "type": "variants",
      "attributes": {
        "uuid": "0c0126de-79cf-4db5-8d2f-875469751755",
        "price": "55.0",
        "line_item_name": "MEMBERSHIP Private Practice",
        "line_item_name_en": "MEMBERSHIP Private Practice",
        "line_item_name_fr": "ADHÉSION Pratique privée",
        "line_item_name_es": "TRANSLATION MISSING: ES.MEMBERSHIP ",
        "type": "VariantMembership",
        "name": "Private Practice",
        "name_en": "Private Practice",
        "name_fr": "Pratique privée",
        "name_es": null,
        "description": "Private Practice Division",
        "description_en": "Private Practice Division",
        "description_fr": "Private Practice Division",
        "description_es": "Private Practice Division",
        "orderable_type_name_en": "Membership",
        "orderable_type_name_fr": "Adhésion",
        "orderable_type_name_es": "translation missing: es.membership",
        "currency": "cad",
        "created_at": "2016-08-04T22:24:33.220Z",
        "updated_at": "2016-08-04T22:24:33.220Z",
        "deleted_at": null,
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true
      },
      "relationships": {
        "interval": {
          "data": {
            "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
            "type": "intervals"
          }
        },
        "orderable": {
          "data": {
            "id": "f1b891a6-c1c3-4483-b2f1-97d26d54e579",
            "type": "memberships"
          }
        }
      }
    },
    {
      "id": "2d83093e-81a1-4877-adca-b7ca0f84ea18",
      "type": "line_items",
      "attributes": {
        "uuid": "2d83093e-81a1-4877-adca-b7ca0f84ea18",
        "quantity": 1,
        "price": "35.0",
        "currency": "cad",
        "amount": "35.0",
        "total": "0.0",
        "subtotal": "0.0",
        "tax_total": "0.0",
        "adjustment_total": "-35.0",
        "manual_adjustment_total": "0.0",
        "promotion_total": "-35.0",
        "interval_total": "0.0",
        "leave_total": "0.0",
        "additional_tax_total": "0.0",
        "included_tax_total": "0.0",
        "updated_at": "2016-10-18T15:34:59.205Z",
        "created_at": "2016-10-18T15:34:33.675Z",
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true,
        "refunded": null
      },
      "relationships": {
        "adjustments": {
          "data": [
            {
              "id": "f3388967-22ea-4a0f-a216-9213f0de3fc2",
              "type": "adjustments"
            }
          ]
        },
        "variant": {
          "data": {
            "id": "f4259a36-2c80-409e-ab21-bb94230a37ef",
            "type": "variants"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "f3388967-22ea-4a0f-a216-9213f0de3fc2",
      "type": "adjustments",
      "attributes": {
        "amount": "-35.0",
        "label": "Student Division Discount",
        "label_en": "Student Division Discount",
        "label_fr": "Student Division Discount",
        "label_es": "Student Division Discount",
        "eligible": true,
        "state": "active",
        "created_at": "2016-10-18T15:34:59.192Z",
        "updated_at": "2016-10-18T15:34:59.192Z",
        "type": "money",
        "percentage": "0.0",
        "source_type": "promotion"
      },
      "relationships": {
        "adjustable": {
          "data": {
            "id": "2d83093e-81a1-4877-adca-b7ca0f84ea18",
            "type": "line_items"
          }
        },
        "source": {
          "data": {
            "id": "475cfd6f-861c-425b-92d6-080fa5c935cf",
            "type": "promotions"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "f4259a36-2c80-409e-ab21-bb94230a37ef",
      "type": "variants",
      "attributes": {
        "uuid": "f4259a36-2c80-409e-ab21-bb94230a37ef",
        "price": "35.0",
        "line_item_name": "MEMBERSHIP Women's Health",
        "line_item_name_en": "MEMBERSHIP Women's Health",
        "line_item_name_fr": "ADHÉSION Santé des femmes",
        "line_item_name_es": "TRANSLATION MISSING: ES.MEMBERSHIP ",
        "type": "VariantMembership",
        "name": "Women's Health",
        "name_en": "Women's Health",
        "name_fr": "Santé des femmes",
        "name_es": null,
        "description": "Women's Health Division",
        "description_en": "Women's Health Division",
        "description_fr": "Women's Health Division",
        "description_es": "Women's Health Division",
        "orderable_type_name_en": "Membership",
        "orderable_type_name_fr": "Adhésion",
        "orderable_type_name_es": "translation missing: es.membership",
        "currency": "cad",
        "created_at": "2016-08-04T22:24:33.547Z",
        "updated_at": "2016-08-04T22:24:33.547Z",
        "deleted_at": null,
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true
      },
      "relationships": {
        "interval": {
          "data": {
            "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
            "type": "intervals"
          }
        },
        "orderable": {
          "data": {
            "id": "d924e554-ef86-445a-a624-d86a3410d9ec",
            "type": "memberships"
          }
        }
      }
    },
    {
      "id": "f2a6dbe5-ce1e-4c8e-8a7d-0d41de019eb9",
      "type": "line_items",
      "attributes": {
        "uuid": "f2a6dbe5-ce1e-4c8e-8a7d-0d41de019eb9",
        "quantity": 1,
        "price": "35.0",
        "currency": "cad",
        "amount": "35.0",
        "total": "0.0",
        "subtotal": "0.0",
        "tax_total": "0.0",
        "adjustment_total": "-35.0",
        "manual_adjustment_total": "0.0",
        "promotion_total": "-35.0",
        "interval_total": "0.0",
        "leave_total": "0.0",
        "additional_tax_total": "0.0",
        "included_tax_total": "0.0",
        "updated_at": "2016-10-18T15:34:59.377Z",
        "created_at": "2016-10-18T15:34:33.730Z",
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true,
        "refunded": null
      },
      "relationships": {
        "adjustments": {
          "data": [
            {
              "id": "031f6e73-e9ca-4784-ad19-97a079dc64d8",
              "type": "adjustments"
            }
          ]
        },
        "variant": {
          "data": {
            "id": "b5045ed3-9c4a-4f57-a5d4-a6f246bd2f8e",
            "type": "variants"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "031f6e73-e9ca-4784-ad19-97a079dc64d8",
      "type": "adjustments",
      "attributes": {
        "amount": "-35.0",
        "label": "Student Division Discount",
        "label_en": "Student Division Discount",
        "label_fr": "Student Division Discount",
        "label_es": "Student Division Discount",
        "eligible": true,
        "state": "active",
        "created_at": "2016-10-18T15:34:59.363Z",
        "updated_at": "2016-10-18T15:34:59.363Z",
        "type": "money",
        "percentage": "0.0",
        "source_type": "promotion"
      },
      "relationships": {
        "adjustable": {
          "data": {
            "id": "f2a6dbe5-ce1e-4c8e-8a7d-0d41de019eb9",
            "type": "line_items"
          }
        },
        "source": {
          "data": {
            "id": "475cfd6f-861c-425b-92d6-080fa5c935cf",
            "type": "promotions"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "b5045ed3-9c4a-4f57-a5d4-a6f246bd2f8e",
      "type": "variants",
      "attributes": {
        "uuid": "b5045ed3-9c4a-4f57-a5d4-a6f246bd2f8e",
        "price": "35.0",
        "line_item_name": "MEMBERSHIP Pain Science",
        "line_item_name_en": "MEMBERSHIP Pain Science",
        "line_item_name_fr": "ADHÉSION Science de la douleur",
        "line_item_name_es": "TRANSLATION MISSING: ES.MEMBERSHIP ",
        "type": "VariantMembership",
        "name": "Pain Science",
        "name_en": "Pain Science",
        "name_fr": "Science de la douleur",
        "name_es": null,
        "description": "Pain Science Division",
        "description_en": "Pain Science Division",
        "description_fr": "Pain Science Division",
        "description_es": "Pain Science Division",
        "orderable_type_name_en": "Membership",
        "orderable_type_name_fr": "Adhésion",
        "orderable_type_name_es": "translation missing: es.membership",
        "currency": "cad",
        "created_at": "2016-08-04T22:24:33.101Z",
        "updated_at": "2016-08-04T22:24:33.101Z",
        "deleted_at": null,
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true
      },
      "relationships": {
        "interval": {
          "data": {
            "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
            "type": "intervals"
          }
        },
        "orderable": {
          "data": {
            "id": "ed6f3051-2742-43f8-bc5b-fe0ab997ed3b",
            "type": "memberships"
          }
        }
      }
    },
    {
      "id": "113ab3c0-bea6-40c4-b660-ad335eaf4831",
      "type": "line_items",
      "attributes": {
        "uuid": "113ab3c0-bea6-40c4-b660-ad335eaf4831",
        "quantity": 1,
        "price": "75.0",
        "currency": "cad",
        "amount": "75.0",
        "total": "0.0",
        "subtotal": "0.0",
        "tax_total": "0.0",
        "adjustment_total": "-75.0",
        "manual_adjustment_total": "0.0",
        "promotion_total": "-75.0",
        "interval_total": "0.0",
        "leave_total": "0.0",
        "additional_tax_total": "0.0",
        "included_tax_total": "0.0",
        "updated_at": "2016-10-18T15:34:59.551Z",
        "created_at": "2016-10-18T15:34:33.784Z",
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true,
        "refunded": null
      },
      "relationships": {
        "adjustments": {
          "data": [
            {
              "id": "0f128417-d2b4-486d-a172-c0037b392397",
              "type": "adjustments"
            }
          ]
        },
        "variant": {
          "data": {
            "id": "df495d64-2459-4b03-b7fe-69bde191839a",
            "type": "variants"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "0f128417-d2b4-486d-a172-c0037b392397",
      "type": "adjustments",
      "attributes": {
        "amount": "-75.0",
        "label": "Student Division Discount",
        "label_en": "Student Division Discount",
        "label_fr": "Student Division Discount",
        "label_es": "Student Division Discount",
        "eligible": true,
        "state": "active",
        "created_at": "2016-10-18T15:34:59.537Z",
        "updated_at": "2016-10-18T15:34:59.537Z",
        "type": "money",
        "percentage": "0.0",
        "source_type": "promotion"
      },
      "relationships": {
        "adjustable": {
          "data": {
            "id": "113ab3c0-bea6-40c4-b660-ad335eaf4831",
            "type": "line_items"
          }
        },
        "source": {
          "data": {
            "id": "475cfd6f-861c-425b-92d6-080fa5c935cf",
            "type": "promotions"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "df495d64-2459-4b03-b7fe-69bde191839a",
      "type": "variants",
      "attributes": {
        "uuid": "df495d64-2459-4b03-b7fe-69bde191839a",
        "price": "75.0",
        "line_item_name": "MEMBERSHIP Sports",
        "line_item_name_en": "MEMBERSHIP Sports",
        "line_item_name_fr": "ADHÉSION Physiothérapie sportive",
        "line_item_name_es": "TRANSLATION MISSING: ES.MEMBERSHIP ",
        "type": "VariantMembership",
        "name": "Sports",
        "name_en": "Sports",
        "name_fr": "Physiothérapie sportive",
        "name_es": null,
        "description": "Sports Division",
        "description_en": "Sports Division",
        "description_fr": "Sports Division",
        "description_es": "Sports Division",
        "orderable_type_name_en": "Membership",
        "orderable_type_name_fr": "Adhésion",
        "orderable_type_name_es": "translation missing: es.membership",
        "currency": "cad",
        "created_at": "2016-08-04T22:24:33.437Z",
        "updated_at": "2016-08-04T22:24:33.437Z",
        "deleted_at": null,
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true
      },
      "relationships": {
        "interval": {
          "data": {
            "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
            "type": "intervals"
          }
        },
        "orderable": {
          "data": {
            "id": "b72456bd-e471-4829-95b9-061cf66e177d",
            "type": "memberships"
          }
        }
      }
    },
    {
      "id": "c6eb6e25-9402-4b27-be26-e557ae88f9ef",
      "type": "line_items",
      "attributes": {
        "uuid": "c6eb6e25-9402-4b27-be26-e557ae88f9ef",
        "quantity": 1,
        "price": "50.0",
        "currency": "cad",
        "amount": "50.0",
        "total": "0.0",
        "subtotal": "0.0",
        "tax_total": "0.0",
        "adjustment_total": "-50.0",
        "manual_adjustment_total": "0.0",
        "promotion_total": "-50.0",
        "interval_total": "0.0",
        "leave_total": "0.0",
        "additional_tax_total": "0.0",
        "included_tax_total": "0.0",
        "updated_at": "2016-10-18T15:34:59.723Z",
        "created_at": "2016-10-18T15:34:33.839Z",
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true,
        "refunded": null
      },
      "relationships": {
        "adjustments": {
          "data": [
            {
              "id": "f76b0dab-5ef0-4e1c-8291-72f475104e99",
              "type": "adjustments"
            }
          ]
        },
        "variant": {
          "data": {
            "id": "034e71eb-57d7-4f31-91e6-fbe77d7522ab",
            "type": "variants"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "f76b0dab-5ef0-4e1c-8291-72f475104e99",
      "type": "adjustments",
      "attributes": {
        "amount": "-50.0",
        "label": "Student Division Discount",
        "label_en": "Student Division Discount",
        "label_fr": "Student Division Discount",
        "label_es": "Student Division Discount",
        "eligible": true,
        "state": "active",
        "created_at": "2016-10-18T15:34:59.709Z",
        "updated_at": "2016-10-18T15:34:59.709Z",
        "type": "money",
        "percentage": "0.0",
        "source_type": "promotion"
      },
      "relationships": {
        "adjustable": {
          "data": {
            "id": "c6eb6e25-9402-4b27-be26-e557ae88f9ef",
            "type": "line_items"
          }
        },
        "source": {
          "data": {
            "id": "475cfd6f-861c-425b-92d6-080fa5c935cf",
            "type": "promotions"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "034e71eb-57d7-4f31-91e6-fbe77d7522ab",
      "type": "variants",
      "attributes": {
        "uuid": "034e71eb-57d7-4f31-91e6-fbe77d7522ab",
        "price": "50.0",
        "line_item_name": "MEMBERSHIP Animal Rehabilitation",
        "line_item_name_en": "MEMBERSHIP Animal Rehabilitation",
        "line_item_name_fr": "ADHÉSION Réadaptation animale",
        "line_item_name_es": "TRANSLATION MISSING: ES.MEMBERSHIP ",
        "type": "VariantMembership",
        "name": "Animal Rehabilitation",
        "name_en": "Animal Rehabilitation",
        "name_fr": "Réadaptation animale",
        "name_es": null,
        "description": "Animal Rehabilitation Division",
        "description_en": "Animal Rehabilitation Division",
        "description_fr": "Animal Rehabilitation Division",
        "description_es": "Animal Rehabilitation Division",
        "orderable_type_name_en": "Membership",
        "orderable_type_name_fr": "Adhésion",
        "orderable_type_name_es": "translation missing: es.membership",
        "currency": "cad",
        "created_at": "2016-08-04T22:24:32.210Z",
        "updated_at": "2016-08-04T22:24:32.210Z",
        "deleted_at": null,
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true
      },
      "relationships": {
        "interval": {
          "data": {
            "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
            "type": "intervals"
          }
        },
        "orderable": {
          "data": {
            "id": "82c1a0d1-e660-4ea9-8183-9bd4408cbea0",
            "type": "memberships"
          }
        }
      }
    },
    {
      "id": "833569cc-630a-4e02-acfb-8ad2c1350a14",
      "type": "line_items",
      "attributes": {
        "uuid": "833569cc-630a-4e02-acfb-8ad2c1350a14",
        "quantity": 1,
        "price": "35.0",
        "currency": "cad",
        "amount": "35.0",
        "total": "0.0",
        "subtotal": "0.0",
        "tax_total": "0.0",
        "adjustment_total": "-35.0",
        "manual_adjustment_total": "0.0",
        "promotion_total": "-35.0",
        "interval_total": "0.0",
        "leave_total": "0.0",
        "additional_tax_total": "0.0",
        "included_tax_total": "0.0",
        "updated_at": "2016-10-18T15:34:59.916Z",
        "created_at": "2016-10-18T15:34:33.894Z",
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true,
        "refunded": null
      },
      "relationships": {
        "adjustments": {
          "data": [
            {
              "id": "10cab856-b315-46b6-bdc2-348e5758cbbc",
              "type": "adjustments"
            }
          ]
        },
        "variant": {
          "data": {
            "id": "94c8c2d4-dc70-485b-acac-4fee9da90327",
            "type": "variants"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "10cab856-b315-46b6-bdc2-348e5758cbbc",
      "type": "adjustments",
      "attributes": {
        "amount": "-35.0",
        "label": "Student Division Discount",
        "label_en": "Student Division Discount",
        "label_fr": "Student Division Discount",
        "label_es": "Student Division Discount",
        "eligible": true,
        "state": "active",
        "created_at": "2016-10-18T15:34:59.901Z",
        "updated_at": "2016-10-18T15:34:59.901Z",
        "type": "money",
        "percentage": "0.0",
        "source_type": "promotion"
      },
      "relationships": {
        "adjustable": {
          "data": {
            "id": "833569cc-630a-4e02-acfb-8ad2c1350a14",
            "type": "line_items"
          }
        },
        "source": {
          "data": {
            "id": "475cfd6f-861c-425b-92d6-080fa5c935cf",
            "type": "promotions"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "94c8c2d4-dc70-485b-acac-4fee9da90327",
      "type": "variants",
      "attributes": {
        "uuid": "94c8c2d4-dc70-485b-acac-4fee9da90327",
        "price": "35.0",
        "line_item_name": "MEMBERSHIP Global Health",
        "line_item_name_en": "MEMBERSHIP Global Health",
        "line_item_name_fr": "ADHÉSION Santé mondiale",
        "line_item_name_es": "TRANSLATION MISSING: ES.MEMBERSHIP ",
        "type": "VariantMembership",
        "name": "Global Health",
        "name_en": "Global Health",
        "name_fr": "Santé mondiale",
        "name_es": null,
        "description": "Global Health Division",
        "description_en": "Global Health Division",
        "description_fr": "Global Health Division",
        "description_es": "Global Health Division",
        "orderable_type_name_en": "Membership",
        "orderable_type_name_fr": "Adhésion",
        "orderable_type_name_es": "translation missing: es.membership",
        "currency": "cad",
        "created_at": "2016-08-04T22:24:32.435Z",
        "updated_at": "2016-08-04T22:24:32.435Z",
        "deleted_at": null,
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true
      },
      "relationships": {
        "interval": {
          "data": {
            "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
            "type": "intervals"
          }
        },
        "orderable": {
          "data": {
            "id": "e3c04df2-212b-457f-8789-68ccf2e2f5a5",
            "type": "memberships"
          }
        }
      }
    },
    {
      "id": "bf1a4795-8260-4c58-b860-5c3843b44a5a",
      "type": "line_items",
      "attributes": {
        "uuid": "bf1a4795-8260-4c58-b860-5c3843b44a5a",
        "quantity": 1,
        "price": "35.0",
        "currency": "cad",
        "amount": "35.0",
        "total": "0.0",
        "subtotal": "0.0",
        "tax_total": "0.0",
        "adjustment_total": "-35.0",
        "manual_adjustment_total": "0.0",
        "promotion_total": "-35.0",
        "interval_total": "0.0",
        "leave_total": "0.0",
        "additional_tax_total": "0.0",
        "included_tax_total": "0.0",
        "updated_at": "2016-10-18T15:35:00.095Z",
        "created_at": "2016-10-18T15:34:33.949Z",
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true,
        "refunded": null
      },
      "relationships": {
        "adjustments": {
          "data": [
            {
              "id": "6292bd3c-41c3-4d5b-b43b-258c45dedffd",
              "type": "adjustments"
            }
          ]
        },
        "variant": {
          "data": {
            "id": "1ceee1e7-7602-4496-abdd-5110baeccce5",
            "type": "variants"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "6292bd3c-41c3-4d5b-b43b-258c45dedffd",
      "type": "adjustments",
      "attributes": {
        "amount": "-35.0",
        "label": "Student Division Discount",
        "label_en": "Student Division Discount",
        "label_fr": "Student Division Discount",
        "label_es": "Student Division Discount",
        "eligible": true,
        "state": "active",
        "created_at": "2016-10-18T15:35:00.080Z",
        "updated_at": "2016-10-18T15:35:00.080Z",
        "type": "money",
        "percentage": "0.0",
        "source_type": "promotion"
      },
      "relationships": {
        "adjustable": {
          "data": {
            "id": "bf1a4795-8260-4c58-b860-5c3843b44a5a",
            "type": "line_items"
          }
        },
        "source": {
          "data": {
            "id": "475cfd6f-861c-425b-92d6-080fa5c935cf",
            "type": "promotions"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "1ceee1e7-7602-4496-abdd-5110baeccce5",
      "type": "variants",
      "attributes": {
        "uuid": "1ceee1e7-7602-4496-abdd-5110baeccce5",
        "price": "35.0",
        "line_item_name": "MEMBERSHIP Paediatrics",
        "line_item_name_en": "MEMBERSHIP Paediatrics",
        "line_item_name_fr": "ADHÉSION Pédiatrie",
        "line_item_name_es": "TRANSLATION MISSING: ES.MEMBERSHIP ",
        "type": "VariantMembership",
        "name": "Paediatrics",
        "name_en": "Paediatrics",
        "name_fr": "Pédiatrie",
        "name_es": null,
        "description": "Paediatrics Division",
        "description_en": "Paediatrics Division",
        "description_fr": "Paediatrics Division",
        "description_es": "Paediatrics Division",
        "orderable_type_name_en": "Membership",
        "orderable_type_name_fr": "Adhésion",
        "orderable_type_name_es": "translation missing: es.membership",
        "currency": "cad",
        "created_at": "2016-08-04T22:24:32.993Z",
        "updated_at": "2016-08-04T22:24:32.993Z",
        "deleted_at": null,
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true
      },
      "relationships": {
        "interval": {
          "data": {
            "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
            "type": "intervals"
          }
        },
        "orderable": {
          "data": {
            "id": "89b287d3-8200-4fde-a0a8-2ed471f67d52",
            "type": "memberships"
          }
        }
      }
    },
    {
      "id": "da7adaa8-2a18-4b9e-ba72-5c8c26f73318",
      "type": "line_items",
      "attributes": {
        "uuid": "da7adaa8-2a18-4b9e-ba72-5c8c26f73318",
        "quantity": 1,
        "price": "0.0",
        "currency": "cad",
        "amount": "0.0",
        "total": "0.0",
        "subtotal": "0.0",
        "tax_total": "0.0",
        "adjustment_total": "0.0",
        "manual_adjustment_total": "0.0",
        "promotion_total": "0.0",
        "interval_total": "0.0",
        "leave_total": "0.0",
        "additional_tax_total": "0.0",
        "included_tax_total": "0.0",
        "updated_at": "2016-10-18T15:34:57.644Z",
        "created_at": "2016-10-18T15:34:34.004Z",
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true,
        "refunded": null
      },
      "relationships": {
        "adjustments": {
          "data": []
        },
        "variant": {
          "data": {
            "id": "deacd894-663e-477b-95fb-347e1329cd76",
            "type": "variants"
          }
        },
        "order": {
          "data": {
            "id": "4ee22704-05d4-4c52-8c25-677a16883764",
            "type": "orders"
          }
        }
      }
    },
    {
      "id": "deacd894-663e-477b-95fb-347e1329cd76",
      "type": "variants",
      "attributes": {
        "uuid": "deacd894-663e-477b-95fb-347e1329cd76",
        "price": "0.0",
        "line_item_name": "MEMBERSHIP Association québécoise de la physiothérapie (AQP) - Entry-level Student",
        "line_item_name_en": "MEMBERSHIP Association québécoise de la physiothérapie (AQP) - Entry-level Student",
        "line_item_name_fr": "ADHÉSION Association québécoise de la physiothérapie (AQP) - ",
        "line_item_name_es": "TRANSLATION MISSING: ES.MEMBERSHIP Association québécoise de la physiothérapie (AQP) - ",
        "type": "VariantMembership",
        "name": "Association québécoise de la physiothérapie (AQP) - Entry-level Student",
        "name_en": "Association québécoise de la physiothérapie (AQP) - Entry-level Student",
        "name_fr": "Association québécoise de la physiothérapie (AQP) - ",
        "name_es": "Association québécoise de la physiothérapie (AQP) - ",
        "description": "Physiotherapy students who do not yet have a License #",
        "description_en": "Physiotherapy students who do not yet have a License #",
        "description_fr": "Physiotherapy students who do not yet have a License #",
        "description_es": "Physiotherapy students who do not yet have a License #",
        "orderable_type_name_en": "Membership",
        "orderable_type_name_fr": "Adhésion",
        "orderable_type_name_es": "translation missing: es.membership",
        "currency": "cad",
        "created_at": "2016-08-04T22:24:30.648Z",
        "updated_at": "2016-08-04T22:24:30.648Z",
        "deleted_at": null,
        "eligible_for_scheduled_payment": true,
        "eligible_for_refund": true,
        "eligible_for_adjustment": true
      },
      "relationships": {
        "interval": {
          "data": {
            "id": "bf65098b-5f52-4eb5-a69b-1d7bc05d8109",
            "type": "intervals"
          }
        },
        "orderable": {
          "data": {
            "id": "091f103d-1371-4054-aa7a-21abb683af13",
            "type": "memberships"
          }
        }
      }
    }
  ]
}
```

This endpoint retrieves a specific order.

### HTTP Request

`GET http://example.com/api/orders/<ID>`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------

# Line Items
# Memberships
# Organizations
# Addresses
# Phones
# Emails
# Payment
# Refund
# Leave
# Intervals
# Tax Rates
# Tax Categories
# Zones
# Donations
# Insurance Options
# Roles
# Fees
# Promotions
# Groups
# Services
# Payment Methods
# Payment Options
# Payment Gateways
# Touchpoints
# Messages
# Comments
# Resource Types
# Queued Jobs
# Search
# Reports / Receipts
# Passwords