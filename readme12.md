# Amazon S3 
it is stands for
Amazon Simple Storage Service is 
  an object 
storage service that provides industry-leading scalability
data availability, security, and performance. 
 we   can 
use Amazon S3 to store any amount of protected  data
 for a range of use cases, 
Amazon S3 provides management features so that you can optimize, organize, and configure access 
to your data because Amazon S3 provides management features.


 ### Amazon S3 Features
 
- Storage classes: that means you can store classes designed for different use cases like data with changing or unknown access patterns .
- Storage management:  that means you can use it to manage costs, meet regulatory requirements, 
reduce latency, and save multiple distinct copies of particular  data 
- Access management: that is means you can audit and manage access to buckets and objects.
- Data processing
 - Storage logging and monitoring

### How it works
because it is object storage that mean it is stores data as objects within buckets. 
- An object is a file and any metadata that describes the file and every object is contained in a bucket. 
- A bucket is a container for objects stored in Amazon S3.

## Getting started to install it in your app
1.  open the project directory and run this command:
> amplify add storage
2. Enter the following when prompted:

> ? Please select from one of the below mentioned services:
    `Content (Images, audio, video, etc.)`
? You need to add auth (Amazon Cognito) to your project in order to add storage for user files. Do you want to add auth now?
    `Yes`
? Do you want to use the default authentication and security configuration?
    `Default configuration`
? How do you want users to be able to sign in?
    `Username`
? Do you want to configure advanced settings?
    `No, I am done.`
? Please provide a friendly name for your resource that will be used to label this category in the project:
    `S3friendlyName`
? Please provide bucket name:
    `storagebucketname`
? Who should have access:
    `Auth and guest users`
? What kind of access do you want for Authenticated users?
    `create/update, read, delete`
? What kind of access do you want for Guest users?
    `create/update, read, delete`
? Do you want to add a Lambda Trigger for your S3 Bucket?
    `No`

3. Add these  into the dependencies :
- implementation 'com.amplifyframework:aws-storage-s3:1.35.4'
 -  implementation 'com.amplifyframework:aws-auth-cognito:1.35.4'
4. Initialize Amplify Storage by add this line to coifiger on create app
- Amplify.addPlugin(new AWSCognitoAuthPlugin());
- Amplify.addPlugin(new AWSS3StoragePlugin());

## Uploading data to your bucket
 > private void uploadFile() {
    File exampleFile = new File(getApplicationContext().getFilesDir(), "ExampleKey");
    try {
        BufferedWriter writer = new BufferedWriter(new FileWriter(exampleFile));
        writer.append("Example file contents");
        writer.close();
    } catch (Exception exception) {
        Log.e("MyAmplifyApp", "Upload failed", exception);
    }
    Amplify.Storage.uploadFile(
            "ExampleKey",
            exampleFile,
            result -> Log.i("MyAmplifyApp", "Successfully uploaded: " + result.getKey()),
            storageFailure -> Log.e("MyAmplifyApp", "Upload failed", storageFailure)
    );
}

resorces:
1. https://docs.amplify.aws/lib/storage/getting-started/q/platform/android/#initialize-amplify-storage
2.  https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html
