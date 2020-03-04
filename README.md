# Adyen OpenAPI / Swagger definitions

Adyen provides [various APIs](https://docs.adyen.com) to help you accept payments on your website or mobile application, implement subscription billing, make payouts, and much more.

This repository contains Adyen API definition files, represented in the [OpenAPI Specification](https://www.openapis.org/) standard (formerly known as Swagger Specification).

## Folder structure

API definitions in this repository are organized into two subfolders:

```
   /json – Definition files in the json format.
   /yaml – Definition files in the yaml format.
```

We support the OpenAPI version 3.0.0.

## Usage
  
There are multiple ways you can use the OpenAPI definition to explore the Adyen API:
-	If you want to see the API definitions in action, visit the [Adyen API Explorer](https://docs.adyen.com/api-explorer/) portal.
-	If you prefer to use the classic Swagger toolset, upload these definitions to the [Swagger Editor](http://editor.swagger.io/) or [SwaggerHub](https://swaggerhub.com/).
-	Also we recommend you use [Postman](https://www.getpostman.com/postman) to import the API definition and create your personal collection of requests.

## Vendor extensions

Adyen's API definitions contain some custom extensions, as [allowed by the OpenAPI standard](https://swagger.io/docs/specification/openapi-extensions/). These are extensions that provide metadata, such as the grouping and sort order of API objects, when they are displayed in the [Adyen API Explorer](https://docs.adyen.com/api-explorer/).

### x-groups

This extension provides a list of all endpoint groups for the selected API.

For example:

```
x-groups:
  - General
  - Modifications
```

### x-groupName and x-sortIndex

These extensions specify how to group endpoints and sort them within a group.

For example:

```
paths:
    ...
    post:
      ...
      x-groupName: Modifications
      x-sortIndex: 5
   ...
```
  
## Support
  
If you have any questions or suggestions, please feel free to [create an issue here](https://github.com/Adyen/adyen-openapi/issues/new) or contact [Adyen Support](https://support.adyen.com).
  
## License 

This repository is open source and available under the MIT license. For more information, see the LICENSE file.

