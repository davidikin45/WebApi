# Building a Web Api

# Verbs
* GET
* POST
* PATCH
* DELETE
* OPTIONS

# Resources
* Nouns. e.g People, Invoices, Payments, Products
* Unit of data that need to be able to manipulate for the business case.
* URIs for path to resource. e.g api.server.com/people
* Query Strings for non-data elements. e.g format, sorting, searching etc.

# Designing Api
* Write down uris
* REST is important but be pragmatic
* Use Dtos to allow for versioning and security.
* associations apis are child collections. e.g /api/camps/123/talks. These can be created as a seperate api.
* Use Options verb and OperationsController for functional actions like refresh-cache. Don't fall into RPC trap.

| Resource | GET | POST | PUT | DELETE |
| ---      | --- | ---  | --- | ---    |
| /custmers| Get List | Create Item | Update Batch | Error |
| /custmers/123| Get Item | Error | Update Item | Delete Item |

# Testing Api
* [Postman](https://www.getpostman.com)

# Versioning Api
* Path. e.g https://api.server.com/api/v1/customers
* Query String e.g htttps://api.server.com/customers?v=2.0
* Headers. e.g X-Version: 2.0
* Accept Headers (Request). e.g Accept: application/json; version=2.0 OR Accept: application/vnd.yourapp.camp.v1+json
* Content Type Headers (Response). e.g Content=Type: application/vnd.yourapp.camp.v1+json

# Dynamic
* By default the dynamic implementation is JObject
