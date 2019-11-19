# Adyen OpenAPI / Swagger specifications

Adyen provides [various APIs](https://docs.adyen.com) to help you accept payments on your website or mobile application, implement subscription billing, make payouts, and much more.

This repository contains Adyen API specifications, represented in the [OpenAPI Specification](https://www.openapis.org/) standard (formerly known as Swagger Specification).

## Folder structure

Specifications in this repository are organized into two subfolders:

```
/specs
   /json – Spec files in the json format.
   /yaml – Spec files in the yaml format.
```

We support the OpenAPI version 3.0.0.

## Usage
  
There are multiple ways you can use the OpenAPI specification to explore the Adyen API:
-	If you want to see the OpenAPI specification in action, visit the [Adyen API Explorer](https://docs.adyen.com/api-explorer/) portal.
-	If you prefer to use the classic Swagger toolset, upload these specifications to the [Swagger Editor](http://editor.swagger.io/) or [SwaggerHub](https://swaggerhub.com/).
-	Also we recommend you use [Postman](https://www.getpostman.com/postman) to import the OpenAPI specification and create your personal collection of requests.

## Vendor extensions

Adyen's specifications contain some custom extensions, as [allowed by the OpenAPI standard](https://swagger.io/docs/specification/openapi-extensions/). These are extensions that provide metadata, such as the grouping and sort order of API objects, when they are displayed in the [Adyen API Explorer](https://docs.adyen.com/api-explorer/).

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

