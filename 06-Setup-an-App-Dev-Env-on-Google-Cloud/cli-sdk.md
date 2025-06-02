# Cloud Storage: Qwik Start - CLI/SDK
    1. Craete a bucket:
      ```bash
      gsutil mb -l europe-west1 gs://student-02-5adb04241e78
      ```
    2. Upload an image to the bucket:
      ```bash
      curl https://upload.wikimedia.org/wikipedia/commons/thumb/a/a4/Ada_Lovelace_portrait.jpg/800px-Ada_Lovelace_portrait.jpg --output ada.jpg
      gcloud storage cp ada.jpg gs://student-02-5adb04241e78
      ```
      Remove the file from your local machine:
      ```bash
      rm ada.jpg
      ```
    3. Download the image from the bucket:
      ```bash
      gcloud storage cp -r gs://student-02-5adb04241e78/ada.jpg .
      ```
    4. Copy an object to a folder in the bucket:
      ```bash
      gcloud storage cp gs://student-02-5adb04241e78/ada.jpg gs://student-02-5adb04241e78/image-folder/
      ```
    5. List objects in the bucket:
      ```bash
      gcloud storage ls gs://student-02-5adb04241e78
      ```
    6. List details for an object:
      ```bash
      gcloud storage ls -l gs://student-02-5adb04241e78/ada.jpg
      ```
    7. Make your object publicly accessible:
      ```bash
      gsutil acl ch -u AllUsers:R gs://student-02-5adb04241e78/ada.jpg
      ```
    8. Remove public access to your object:
      ```bash
      gsutil acl ch -d AllUsers gs://student-02-5adb04241e78/ada.jpg
      ```
    9. Delete an object:
      ```bash
      gcloud storage rm gs://student-02-5adb04241e78/ada.jpg
      ```