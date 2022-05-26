# Amplify and Cognito

## Amplify AUTHENTICATION
 we can use the Amplify Auth category  in case we need to authentication because it provides an interface for 
 authenticating a user
 and in the backend it provide  the necessary authorization to the other Amplify categories
 
### Prerequisites
> An Android application targeting at least Android SDK API level 16 with Amplify libraries integrated


### Configure Auth Category
we must follow some step to configure it

1. open the project directory then enter this command 
 >amplify add auth
2. Enter the following when prompted:
3. >? Do you want to use the default authentication and security configuration?
   

-  `Default configuration`

>  ? How do you want users to be able to sign in?

-  `Username`

>   ? Do you want to configure advanced settings?

- `No, I am done.`

4. then push the changes by enter this command
- amplify push

5. Install Amplify Libraries  by add the following dependency on app's __build.gradle__ then  click __Sync Now__
>implementation 'com.amplifyframework:aws-auth-cognito:1.35.4'

6.Initialize Amplify Auth by adding the Auth plugin before calling __Amplify.configure__
>// Add this line, to include the Auth plugin.

>Amplify.addPlugin(new AWSCognitoAuthPlugin());

>Amplify.configure(getApplicationContext());

7. Check the current auth session by run following thine  in MainActivity's onCreate method.

>Amplify.Auth.fetchAuthSession(
result -> Log.i("AmplifyQuickstart", result.toString()),
error -> Log.e("AmplifyQuickstart", error.toString())
);

## Sign in

### Prerequisites
- Amplify AUTHENTICATION
 ### Register a user
- Add the following api to initiate a sign up flow
> AuthSignUpOptions options = AuthSignUpOptions.builder()
.userAttribute(AuthUserAttributeKey.email(), "my@email.com")
.build();
Amplify.Auth.signUp("username", "Password123", options,
result -> Log.i("AuthQuickStart", "Result: " + result.toString()),
error -> Log.e("AuthQuickStart", "Sign up failed", error)
);

- now  tou must confirm the user Enter the confirmation code received via email in the confirmSignUp call.
 > Amplify.Auth.confirmSignUp(
 "username",
 "the code you received via email",
 result -> Log.i("AuthQuickstart", result.isSignUpComplete() ? "Confirm signUp succeeded" : "Confirm sign up not complete"),
 error -> Log.e("AuthQuickstart", error.toString())
 );

- if you see the following in your console window that mean successfully done:
> Confirm signUp succeeded

### Sign in a user
- get the username and password from the user using by bulid UI for that. 
- After the user enters the username and password you can start the sign in flow by calling the following method:
 > Amplify.Auth.signIn(
 "username",
 "password",
 result -> Log.i("AuthQuickstart", result.isSignInComplete() ? "Sign in succeeded" : "Sign in not complete"),
 error -> Log.e("AuthQuickstart", error.toString())
 );

- if you see in windows termainal  this line than mean all thing ok
> Sign in succeeded
 ## Things I want to know more about

-I would like to learn more about  authentication and how to do that in more  detail


resources:
[resources] (https://docs.amplify.aws/lib/auth/getting-started/q/platform/android/)


