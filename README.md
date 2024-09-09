<p align="center">
  <img src="https://firebase.google.com/static/downloads/brand-guidelines/SVG/logo-standard.svg" />
</p>
<p align="center">
  <img src="https://cdn2.hubspot.net/hubfs/439485/Official_Logos/RESTful-API-logo-for-light-bg.png#keepProtocol" width="50%" />
</p>

</br>

## REALTIME DATABASE 🗄️

</br>

**_🚀 Get list data (method : GET) :_**

```js
https://{projectID}-default-rtdb.firebaseio.com/{listName}.json
```

</br>

**_🚀 Delete list data (method : DELETE) :_**

```js
https://{projectID}-default-rtdb.firebaseio.com/{listName}.json
```

</br>

**_🚀 Post data (method : POST) :_**

```js
https://{projectID}-default-rtdb.firebaseio.com/{listName}.json
```

</br>

**Body**

```js
{
    "email": "xxxx@gmail.com",
    "password": "xxxxxx"
    .
    .
    .
}
```

</br>

**_🚀 Get, Update, Delete data (methods : GET, PUT, DELETE) :_**

```js
https://{projectID}-default-rtdb.firebaseio.com/{listName}/{dataID}.json
```

</br>

**Body (only PUT method)**

```js
{
    "email": "xxxx@gmail.com",
    "password": "xxxxx"
    .
    .
    .
}
```

</br>

## FIRESTORE DATABASE 🗄️

<br/>

**_🚀 Get all documents (method : GET) :_**

```js
https://firestore.googleapis.com/v1/projects/{YOUR_PROJECT_ID}/databases/(default)/documents/{YOUR_COLLECTION}
```

</br>

**_🚀 Get document (method : GET) :_**

```js
https://firestore.googleapis.com/v1/projects/{YOUR_PROJECT_ID}/databases/(default)/documents/{YOUR_COLLECTION}/{DOCUMENT_ID}
```

</br>

**_🚀 Post document (method : POST, random id) :_**

```js
https://firestore.googleapis.com/v1/projects/{YOUR_PROJECT_ID}/databases/(default)/documents/{YOUR_COLLECTION}
```

</br>

**Body**

```js
{
  "fields": {
    "email": {
      "stringValue": "xxxx@example.com"
    },
    "password": {
      "stringValue": "xxxxx"
    },
    .
    .
    .
  }
}
```

<br/>

**_🚀 Post document (method : POST (PATCH), create a document with the name you want)_**

```js
https://firestore.googleapis.com/v1/projects/{YOUR_PROJECT_ID}/databases/(default)/documents/{YOUR_COLLECTION}/{DOCUMENT_ID}
```

</br>

**Body**

```js
{
  "fields": {
    "email": {
      "stringValue": "xxxx@example.com"
    },
    "password": {
      "stringValue": "xxxxx"
    },
    .
    .
    .
  }
}
```

</br>

**_🚀 Update document (method : PUT (PATCH)) :_**

```js
https://firestore.googleapis.com/v1/projects/{YOUR_PROJECT_ID}/databases/(default)/documents/{YOUR_COLLECTION}/{DOCUMENT_ID}
```

</br>

**Body**

```js
{
  "fields": {
    "email": {
      "stringValue": "xxxx@example.com"
    },
    "password": {
      "stringValue": "xxxxx"
    },
    .
    .
    .
  }
}
```

</br>

**_🚀 Delete document (method : DELETE) :_**

```js
https://firestore.googleapis.com/v1/projects/{YOUR_PROJECT_ID}/databases/(default)/documents/{YOUR_COLLECTION}/{DOCUMENT_ID}
```

</br>

## AUTHENTICATION 🔐

<br/>

**_🚀 Register (method : POST) :_**

```js
https://identitytoolkit.googleapis.com/v1/accounts:signUp?key=[API_KEY]
```

<br/>

**Body**

```js
{
    "email": "xxxx@gmail.com",
    "password": "xxxxxxxx",
    "displayName": "xxxx",
    "returnSecureToken": true
}
```

</br>
 
 ***🚀 Login (method : POST) :***

```js
https://identitytoolkit.googleapis.com/v1/accounts:signInWithPassword?key=[API_KEY]
```

</br>

**Body**

```js
{
    "email": "xxxx@gmail.com",
    "password": "xxxxxxxx",
    "returnSecureToken": true
}
```

</br>

**_🚀 Update email (method : POST) :_**

```js
https://identitytoolkit.googleapis.com/v1/accounts:update?key=[API_KEY]
```

</br>

**Body**

```js
{
    "idToken": "xxxxx",
    "email": "xxxxx@gmail.com", // new email
    "returnSecureToken": true
}
```

</br>

**_🚀 Update password (method : POST) :_**

```js
https://identitytoolkit.googleapis.com/v1/accounts:update?key=[API_KEY]
```

</br>

**Body**

```js
{
    "idToken": "xxxxx",
    "password": "xxxxxxxxx", // new password
    "returnSecureToken": true
}
```

</br>

**_🚀 Update account (method : POST) :_**

```js
https://identitytoolkit.googleapis.com/v1/accounts:update?key=[API_KEY]
```

</br>

**Body**

```js
{
    "idToken": "xxxxx",
    "displayName": "xxxxx",
    "photoUrl" : "xxxxx",
    // "deleteAttribute": ["DISPLAY_NAME", "PHOTO_URL"],  // List attributes to delete
    "returnSecureToken": true
}
```

</br>

**_🚀 Delete user (method : DELETE) :_**

```js
https://identitytoolkit.googleapis.com/v1/accounts:delete?key=[API_KEY]
```

</br>

**Body**

```js
{
    "idToken": "xxxxx",
}
```

</br>

**_🚀 Get user info (method : POST) :_**

```js
https://identitytoolkit.googleapis.com/v1/accounts:lookup?key=[API_KEY]
```

</br>

**Body**

```js
{
    "idToken": "xxxxx"
}
```

</br>

## STORAGE 📦

<br/>

**_🚀 Upload image (method : POST) :_**

```js
https://firebasestorage.googleapis.com/v0/b/{projectID}.appspot.com/o/{folderName}%2F{pictureName}.png
```

<br/>

**Body**

```js
file; // Image File
```

<br/>

**Headers**

```js
{
    headers: {
        "Content-Type": file.type
    }
}
```

<br/>

**_🚀 Update image (method : POST) :_**

```js
https://firebasestorage.googleapis.com/v0/b/{projectID}.appspot.com/o/{folderName}%2F{pictureName}.png
```

<br/>

**Body**

```js
file; // Image File
```

<br/>

**Headers**

```js
{
    headers: {
        "Content-Type": file.type
    }
}
```

<br/>

**_🚀 Delete image (method : DELETE) :_**

```js
https://firebasestorage.googleapis.com/v0/b/{projectID}.appspot.com/o/{folderName}%2F{pictureName}.png
```

<br/>

**_🚀 Get image info (method : GET) :_**

```js
https://firebasestorage.googleapis.com/v0/b/{projectID}.appspot.com/o/{folderName}%2F{pictureName}.png
```

<br/>

**_🚀 Image url :_**

```js
https://firebasestorage.googleapis.com/v0/b/{projectID}.appspot.com/o/{folderName}%2F{pictureName}.png?alt=media&token={imageDownloadToken}
```
