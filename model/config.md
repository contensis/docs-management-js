
# Config 

It represents the client API configuration.

## Properties

| Name           | Type   | Format                | Description                             |
|----------------|--------|-----------------------|-----------------------------------------|
| rootUrl?       | string |                       | The root url of the Contensis instance |
| projectId?     | string |                       | The Contensis project id               |
| clientId?      | string |                       | The client id value taken from the API key created in Contensis |
| clientSecret?  | string |                       | The client id value taken from the API key created in Contensis |
| language?      | string |                       | The default language                    |
| versionStatus? | string | 'latest', 'published' | The version status of the items retrieved by the API calls. The default value is *latest* |
| pageIndex?     | number |                       | The page index for the items retrieved by the API calls. The default value is *0* |
| pageSize?      | number |                       | The page size of the items retrieved by the API calls. The default value is *25* |