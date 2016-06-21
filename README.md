# Social-Signin-Android

This provides easy to implement helper classes for diffrent third party logins.

###This social login includes following third party logins:
* Sign in with **Google**
* Sign in with **Google plus**
* Sign in with **LinkedIn**
* Sign in with **Facebook**
* Sign in with **Twiiter**

###How to use it? *(This is general procedure for any third party signin)*
* Create project in respective developer site and get key/credentials for authentication.
* In `inCreate()` method of your login activity/fragment, initilize the helper class. Here is an example of google plus authentication. e.g. 
  ```mGHelper = new GooglePlusSignInHelper(this, this);```
* Implement callback listener. e.g. 
  ```public class MainActivity extends AppCompatActivity implements GoogleResponseListener{
      ...```
* In `onClickListner()` of your button call `performSignIn()` method. e.g. 
  ```  case R.id.g_plus_login_btn:
                mGHelper.performSignIn();
                break;```
* In `onActivityResult()` of your fragment/acivity call `onActivityResult()` of your respective helper class. e.g.
  ```mGHelper.onActivityResult(requestCode, resultCode, data);```

###What if I want to implement single third party signin.
* If you don't want to implement all the sign in functionality just copy respective helper package into you project and follow the same procedure as mentioned above.
 
###List of helper packages:
* Google Signin -> **googleAuthSignin**
* Google Plus Signin -> **googleSignIn**
* Facebook Signin -> **facebookSignIn**
* LinedIn signin -> **linkedInSiginIn**
* Twitter signin -> **twitterSignIn**
