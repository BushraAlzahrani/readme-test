# Flutter Template

There are **five features**  with fully **customizable theme**. The used databse is **firebase** to strat using the template you need to enable the following in firebase:
Authentication, firestore and storage.

##  Features

### **1. Splash Screen**

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

**	The user functionalities:**
-  View products
- Search products
- Add or delete product to/from cart
- Add or delete product to/from favorite

**	The Admin functionalities:**
-  View user information
- Edit  user information
- Edit password 
- Logout

### **5. Current Location**
The current location works on android ios, and web. To activate it you need to add the api key for google map in each one.

**	Android:**

In your flutter project go to the **androidmanifest.xml** file by following this path *android/app/main/androirdmanifest.xml*. In the 10th line add the api key:
```xml
<meta-data android:name="com.google.android.geo.API_KEY" android:value="YOUR_KEY"/>
```

**	IOS:**

In your flutter project go to **AppDelegate.swift** file  by following this path *ios/runner/AppDelegate.swift*. In the 11th line add the api key:

```swift
GMSServices.provideAPIKey("YOUR_KEY")
```

**	Web**

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



## Theme



