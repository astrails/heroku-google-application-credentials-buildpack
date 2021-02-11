# heroku-google-application-credentials-buildpack
Generates a Google credential file based on Heroku Config Vars.

This is useful when using a package such as [@google-cloud/storage](https://www.npmjs.com/package/@google-cloud/storage) which loads credentials from a file instead of an environmental variable.

## Usage

1. Create Config Vars key `GOOGLE_CREDENTIALS` and `GOOGLE_CONTENT_API_KEY` paste the content of service account credential JSON file as is.
2. There is no #2.

Config Var `GOOGLE_APPLICATION_CREDENTIALS` will be used to create `google-credentials.json`.

Config Var `GOOGLE_CONTENT_API_KEY` will be used to create `content-api-key.json`.

The script with generate a file called `google-credentials.json` and `content-api-key.json` which holds the key from the step #1 above.
