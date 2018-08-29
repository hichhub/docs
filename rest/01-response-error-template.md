- Feature Name: Response Error Template
- Create Date: 2018-08-29 14:17:23
- Modification Date: 2018-08-29 14:17:23
- Version: 1.0.0

# Summary
This is an RFC to format all responses which includes an error in a specified template.

# Motivation
In our technical team, we decided to consider a specific template for all of the responses we serve any API's endpoint. Also, This document will help the newcomer developers to adapt themselves with our technical vision and culture.

# Detailed design
Response's body will be a serialized JSON object which includes some keys as the following table.

| Key            | Value                                             | Data Type |
|----------------|---------------------------------------------------|-----------|
| parameter_name | an array of objects which consists list of errors | list      |

#### Error list JSON schema
```json
{
  "paramter_name": [
    {
      "code": 100,
      "message": "this is error message"
    }
  ]
}
```


#### Example
```json
{
  "first_name": [
    {
      "code": 100,
      "message": "Length of the first name is longer than 20 character"
    },
    {
      "code": 101,
      "message": "First name must be capitalized"
    },
    ...
  ]
}
```
