# api-docs

## Generate API key
User will need to generate an API key that will identify him when doing API requests. The key will be valid for 180 days and can be revoked by the user at any time.
User needs to have sufficient credit balance to perform the API request, if there is no output generated credits will not be deducted.

The user can generate key and see API example use in the app if a given Dazbog feature supports API calls.

## API overview
API is available at POST https://us-central1-vaibe-374418.cloudfunctions.net/api the headers need to include:

```
  'x-api-key': user_generated_api_key,
  'Content-Type': 'application/json'
```

The body will always include

```
  'model': unique_id_of_the_feature
```

and usually prompt and / or absolute URLs of input images.

The output will contain URLs of the generated images.

## Latency
Based on the model latency may vary but should be more or less the same as when using the feature in APP.
