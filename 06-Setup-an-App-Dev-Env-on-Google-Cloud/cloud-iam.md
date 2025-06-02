# Cloud IAM: Qwik Start
1. Explore the IAM console and project level roles
  Return to the Username 1 Cloud Console page.
  Select Navigation menu > IAM & Admin > IAM. You are now in the "IAM & Admin" console.
  Click +GRANT ACCESS button at the top of the page.
  Scroll down to Basic in Select a role section and mouse over.
  There are three roles:
    Editor
    Owner
    Viewer

2. Create a bucket
  Create a Cloud Storage bucket with a unique name. From the Cloud Console, select Navigation menu > Cloud Storage > Buckets.

  Click +CREATE.

3. Remove project access
  Switch to the Username 1 console.

  Remove Project Viewer for Username 2
  Select Navigation menu > IAM & Admin > IAM. Then click the pencil icon inline and to the right of Username 2.
  Note: You may have to widen the screen to see the pencil icon.
  Remove Project Viewer access for Username 2 by clicking the trashcan icon next to the role name. Then click SAVE.

4. Add Cloud Storage permissions
  Copy Username 2 name from the Lab Connection panel.

  Switch to Username 1 console. Ensure that you are still signed in with Username 1's credentials. If you are signed out, sign in back with the proper credentials.

  In the Console, select Navigation menu > IAM & Admin > IAM.

  Click +GRANT ACCESS button and paste the Username 2 name into the New principals field.

  In the Select a role field, select Cloud Storage > Storage Object Viewer from the drop-down menu.

  Click SAVE.

5. Verify access
  Switch to the Username 2 console. You'll still be on the Storage page.
  Username 2 doesn't have the Project Viewer role, so that user can't see the project or any of its resources in the Console. However, this user has specific access to Cloud Storage, the Storage Object Viewer role - check it out now.

  Click Activate Cloud Shell the icon that activates cloud shell to open the Cloud Shell command line. If prompted click Continue.

  Open up a Cloud Shell session and then enter in the following command, replace [YOUR_BUCKET_NAME] with the name of the bucket you created earlier:

  gsutil ls gs://[YOUR_BUCKET_NAME]