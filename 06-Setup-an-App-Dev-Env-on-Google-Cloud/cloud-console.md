# Cloud Storage: Qwik Start - Cloud Console
  To create a bucket:
    1. In the Cloud console, go to Navigation menu (Navigation menu) > Cloud Storage > Buckets.
    2. Click + Create:
    3. Enter your bucket information and click Continue to complete each step:
      - Name your bucket: Enter a unique name for your bucket. For this lab, you can use your Project ID as the bucket name because it will always be unique.
      - Bucket naming rules:
        - Do not include sensitive information in the bucket name, because the bucket namespace is global and publicly visible.
        - Bucket names must contain only lowercase letters, numbers, dashes (-), underscores (_), and dots (.). Names containing dots require verification.
        - Bucket names must start and end with a number or letter.
        - Bucket names must contain 3 to 63 characters. Names containing dots can contain up to 222 characters, but each dot-separated component can be no longer than 63 characters.
        - Bucket names cannot be represented as an IP address in dotted-decimal notation (for example, 192.168.5.4).
        - Bucket names cannot begin with the "goog" prefix. Bucket names cannot contain "google" or close misspellings of "google".*
        - Also, for DNS compliance and future compatibility, you should not use underscores (_) or have a period adjacent to another period or dash. For example, ".." or "-." or ".-" are not valid in DNS names.

      - Choose Region for Location type and europe-west1 for Location.
      - Choose Standard for default storage class.
      - Choose Uniform for Access control and uncheck Enforce public access prevention on this bucket to turn it off.
      - Leave the rest of the fields as their default values and click Create.

    3. To upload the image above into your new bucket:
      - Right-click on the image above and download it to your computer. Save the image as kitten.png, renaming it on download.
      - In the Cloud Storage browser page, click the name of the bucket that you created.
      - In the Objects tab, click Upload > Upload files.
      - In the file dialog, go to the file that you downloaded and select it.

    4. To allow public access to the bucket and create a publicly accessible URL for the image:
      - Click the Permissions tab above the list of files.
      - Ensure the view is set to Principals. Click Grant Access to view the Add principals pane.
      - In the New principals box, enter allUsers.
      - In the Select a role drop-down, select Cloud Storage > Storage Object Viewer.
      - Click Save.
      - In the Are you sure you want to make this resource public? window, click Allow public access.

    5. Create folders
      - In the Objects tab, click Create folder.
      - Enter folder1 for Name and click Create.
      - You should see the folder in the bucket with an image of a folder icon to distinguish it from objects.
      - Create a subfolder and upload a file to it:
        Click folder1.
        Click Create folder.
        Enter folder2 for Name and click Create.
      Click folder2.
      Click Upload > Upload files.

    6. Delete a folder
      - Click the arrow next to Bucket details to return to the buckets level.
      - Select the bucket.
      - Click on the Delete button.
      - In the window that opens, type DELETE to confirm the deletion of the folder.
      - Click Delete to permanently delete the folder and all objects and subfolders in it.