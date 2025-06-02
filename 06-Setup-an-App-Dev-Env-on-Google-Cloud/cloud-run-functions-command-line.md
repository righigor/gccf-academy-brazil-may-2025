# Cloud Run Functions: Qwik Start - Command Line

1. Create a function
  - In Cloud Shell, run the following command to set the default region:
    ```bash
    gcloud config set run/region us-central1
    ```
  - Create a directory for your function:
    ```bash
    mkdir hello-function
    cd hello-function
    ```
  - Create and open index.js to edit:
    ```bash
    nano index.js
    ```
  - Copy the following into the index.js file:
    ```bash
      const functions = require('@google-cloud/functions-framework');
      functions.cloudEvent('helloPubSub', cloudEvent => {
      const base64name = cloudEvent.data.message.data;

      const name = base64name
        ? Buffer.from(base64name, 'base64').toString()
        : 'World';

      console.log(`Hello, ${name}!`);
    });
    ```
2. Deploy the function
  - Deploy the nodejs-pubsub-function function to a pub/sub topic named cf-demo
    ```bash
      gcloud functions deploy nodejs-pubsub-function \
        --gen2 \
        --runtime=nodejs20 \
        --region=REGION \
        --source=. \
        --entry-point=helloPubSub \
        --trigger-topic cf-demo \
        --stage-bucket PROJECT_ID-bucket \
        --service-account cloudfunctionsa@PROJECT_ID.iam.gserviceaccount.com \
        --allow-unauthenticated
    ```
  - Verify the status:
    ```bash
    gcloud functions describe nodejs-pubsub-function \
  --region=REGION 
    ```