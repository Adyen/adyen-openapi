# Adyen OpenAPI / Swagger specifications

Adyen provides you with [plenty of different APIs](https://docs.adyen.com/developers) that help you accept payments on your website or mobile application, implement subscription billing, make payouts, and much more.

This repository contains Adyen API specifications, represented in the [OpenAPI standard](https://www.openapis.org/) (former Swagger specification).

## Folder structure

All specifications in this repository are organized into two subfolders:

```
/specs
   /2.0 – Spec files in the OpenAPI 2.0 format.
   /3.0 – Spec files in the OpenAPI 3.0.0 format.
```

We provide specifications in both `.json` and `.yaml` formats, with an API version number (e.g. `v30`) in a file name.

## Usage
  
There are multiple ways you can use the OpenAPI specification to explore the Adyen API:
-	If you want to see the OpenAPI specification in action, visit the [Adyen API Explorer](https://docs.adyen.com/api-explorer/) portal.
-	If you prefer to use the classic Swagger toolset, upload these specifications to the [Swagger Editor](http://editor.swagger.io/) or [SwaggerHub](https://swaggerhub.com/).
-	Also we recommend you use [Postman](https://www.getpostman.com/postman) to import the OpenAPI specification and create your personal collection of requests.

## Custom extensions

Adyen specifications contain a few custom extensions, which are [allowed by the OpenAPI standard](https://swagger.io/docs/specification/openapi-extensions/). These extensions are used to provide metadata about API objects, for instance, to set grouping and sort order when displaying them in the [Adyen API Explorer](https://docs.adyen.com/api-explorer/).

For example:

```
"x-groups" : [
   "General",
   "Modifications"
],

   "post" : {
       "x-groupName" : "Modifications",
       "x-sortIndex" : 5,
```

  
## Support
  
If you have any questions or suggestions, please feel free to create an issue here or contact [Adyen Support](https://support.adyen.com).
  
## License 

This repository is open source and available under the MIT license. For more information, see the LICENSE file.

