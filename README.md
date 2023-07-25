# Adyen OpenAPI / Swagger definitions

Adyen provides [various APIs](https://docs.adyen.com) to help you accept payments on your website or mobile application, implement subscription billing, make payouts, and much more.

This repository contains Adyen API definition files, represented in the [OpenAPI Specification](https://www.openapis.org/) standard (formerly known as Swagger Specification).

## Folder structure

API definitions in this repository are organized into two sub-folders:

```
   /json – Definition files in the json format.
   /yaml – Definition files in the yaml format.
```

We support the OpenAPI version 3.1.0.

## Usage
  
There are multiple ways you can use the OpenAPI definition to explore the Adyen API:
-	If you want to see the API definitions in action, visit the [Adyen API Explorer](https://docs.adyen.com/api-explorer/) portal.
-	If you prefer to use the classic Swagger toolset, upload these definitions to the [Swagger Editor](http://editor.swagger.io/) or [SwaggerHub](https://swaggerhub.com/).
-	Also, we recommend you use [Postman](https://www.getpostman.com/postman) to import the API definition and create your personal collection of requests.

## Vendor extensions

Adyen's API definitions contain some custom extensions, as [allowed by the OpenAPI standard](https://swagger.io/docs/specification/openapi-extensions/). These are extensions that provide metadata, such as the grouping and sort order of API objects, when they are displayed in the [Adyen API Explorer](https://docs.adyen.com/api-explorer/).

### x-groups

This extension provides a list of all endpoint groups for the selected API.

For example:

``` yaml
x-groups:
  - General
  - Modifications
```

### x-groupName and x-sortIndex

These extensions specify how to group endpoints and sort them within a group.

For example:

``` yaml
paths:
    ...
    post:
      ...
      x-groupName: Modifications
      x-sortIndex: 5
   ...
```

### x-publicVersion

This is an auxiliary extension that helps us verify that the current API version is publicly available.

### x-addedInVersion, x-deprecatedInVersion and x-deprecatedMessage

These extensions help us add information when a certain endpoint or field has been added, and later when they are deprecated. 

In addition, the `x-deprecatedMessage` can contain a human-readable message explaining what to use instead of a deprecated API, which provides much better developer experience:

``` yaml
        recurringDetailReference:
          deprecated: true
          x-deprecatedInVersion: 49
          x-deprecatedMessage: Use `storedPaymentMethodId` instead.
          description: This is the `recurringDetailReference` returned in the response when you created the token.
          type: string
        storedPaymentMethodId:
          x-addedInVersion: 49
          description: This is the `recurringDetailReference` returned in the response when you created the token.
          type: string
```

### x-oneOf, x-anyOf, x-not and x-allOf

These extensions are equivalent to those from the [JSON Schema](https://json-schema.org/understanding-json-schema/reference/combining.html) but don't enforce strict validation.

We use them in some rare cases when we need to avoid validation issues with open-source tooling, while still being able to display this information in our [API Explorer](https://docs.adyen.com/api-explorer/).

## Support
  
If you have a feature request, or spotted a bug or a technical problem, create a GitHub issue. For other questions, contact our [Team](https://www.adyen.help/hc/en-us/requests/new).
  
## License 

This repository is open source and available under the MIT license. For more information, see the LICENSE file.

