# Flutter Template

There are **five features**  with fully **customizable theme**. The used databse is **firebase** to start using the template you need to enable the following in firebase:
Authentication, firestore and storage. The used state management **Getx**.

##  Features

### **1. Splash Screen**
The splash screen is the first screen which will transition to your app itself. Usually it includes the app logo.

### **2. Authentication**

The authentication includes three ways to register or login:
-  Google
- Phone Number
- Password & Email

### **3. Profile**

The user profile includes the follwing functionalities:
- View user information
- Edit  user information
- Edit password 
- Logout

### **4. CRUD**

The crud (create, read, update, delete) has two roles a user and admin each has thier own functionalities.

**The user functionalities:**
-  View products
- Search products
- Add or delete product to/from cart
- Add or delete product to/from favorite

**The Admin functionalities:**
-  View user information
- Edit  user information
- Edit password 
- Logout

### **5. Current Location**
The current location works on android ios, and web. To activate it you need to add the api key for google map in each one.

**Android:**

In your flutter project go to the **androidmanifest.xml** file by following this path *android/app/main/androirdmanifest.xml*. In the 10th line add the api key:
```xml
<meta-data android:name="com.google.android.geo.API_KEY" android:value="YOUR_KEY"/>
```

**IOS:**

In your flutter project go to **AppDelegate.swift** file  by following this path *ios/runner/AppDelegate.swift*. In the 11th line add the api key:

```swift
GMSServices.provideAPIKey("YOUR_KEY")
```

**Web**

In your flutter project go to **index.html** file  by following this path *web/index.html*. In the 35th line add the api key:

```html
<script src="https://maps.googleapis.com/maps/api/js?key=YOUR_KEY"></script>
```
To enable Api do this
1. Go to API Manager
2. Click on Overview
3. Search for Google Maps JavaScript API(Under Google Maps APIs). Click on that
4. You will find Enable button there. Click to enable API.
OR You can try this url: [Maps JavaScript API](http://console.cloud.google.com/apis/library/maps-backend.googleapis.com?q=Google%20Maps%20JavaScript%20API&id=fd73ab50-9916-4cde-a0f6-dc8be0a0d425&project=windy-furnace-180806&pli=1 "Maps JavaScript API")



##  Folder Structure
The template follows the feature pattern with Getx state management. the main folders are: common core and featuers. 

### 1. Common:

Includes the widgets which are common betweenfeatures.

### 2. Core

The core folder consists of the following folders. 

** a. binding: **

Includes the dependency injection for all the controllers.

** b. constants: **

Includes all the strings that will be used often throught the app which are the image pathes, the firbase collections the keys for the getx storage the screen sizes and finally the validation format to handel the user input e.g email.

** c. db: **

The database folder is where the firebase instances are initailzed which are Firebase Auth, Firebase Firestore and Firebase Storage.

** d. localization:**

The localization is where the translation is done it has tow languages Arabic and English each language has its' own file consisting of all the app text written as a map the key is shared between the languages and the value is the translation.

** e. responsive:**

Includes the devices sizes which are mobile, larage mobile, tablet and desktop.

** f. routes:**

Includes all the app screens route.
** g. themes:**

All the flutter widgets styles from color to sizes are included in themes folder.  This folder can be taken in another project with or without any state management, and it will apply the theme you have in your flutter app project, all you need to do is add the theme controller in your **main.dart** like so: 
```dart
themeMode: ThemeController().themeDataGet,
theme: ThemeApp.lightTheme,
darkTheme: ThemeApp.darkTheme,
```


### 3. Featuers

The feature folder consists of the features mentioned above as the main folders and each includes three folders logic, model, and view. First, the logic consists of all the logical solutions for said feature in two sub-folders the first one is the controller which is the place where you write all the functions you need for your project. the second folder in logic is the service it is where the connection and data manipulation of the firebase database is done. The second main folder in a feature folder is the model which is the structure of the data for a said feature, this folder is excluded from the features Authentication and google map as it was unnecessary for them, because for the authentication the structure of the user data is already provided from firebase authentication and as for google map there was no mean to save its data to firebase which is the user current location. Lastly the view folder which has tow sub-folders screen and widget.




