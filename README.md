<p align="center">
  <img src="https://firebase.google.com/static/downloads/brand-guidelines/SVG/logo-standard.svg" />
</p>
<p align="center">
  <img src="https://cdn2.hubspot.net/hubfs/439485/Official_Logos/RESTful-API-logo-for-light-bg.png#keepProtocol" width="50%" />
</p>

</br>

# REALTIME DATABASE 💾

</br>

### 🚀 Get list data (method : GET) :

```js
https://{projectID}-default-rtdb.firebaseio.com/{listName}.json
```

</br>

### 🚀 Delete list data (method : DELETE) :

```js
https://{projectID}-default-rtdb.firebaseio.com/{listName}.json
```

</br>

### 🚀 Post data (method : POST) :

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

### 🚀 Get data (method : GET) :

```js
https://{projectID}-default-rtdb.firebaseio.com/{listName}/{dataID}.json
```

</br>

### 🚀 Delete data (method : DELETE) :

```js
https://{projectID}-default-rtdb.firebaseio.com/{listName}/{dataID}.json
```

</br>

### 🚀 Update data (method : PUT) :

```js
https://{projectID}-default-rtdb.firebaseio.com/{listName}/{dataID}.json
```

</br>

**Body**

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

# FIRESTORE DATABASE 🗄️

<br/>

### 🚀 Get all documents (method : GET) :

```js
https://firestore.googleapis.com/v1/projects/{YOUR_PROJECT_ID}/databases/(default)/documents/{YOUR_COLLECTION}
```

</br>

### 🚀 Get document (method : GET) :

```js
https://firestore.googleapis.com/v1/projects/{YOUR_PROJECT_ID}/databases/(default)/documents/{YOUR_COLLECTION}/{DOCUMENT_ID}
```

</br>

### 🚀 Post document (method : POST, random id) :

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

### 🚀 Post document (method : POST (PATCH), create a document with the name you want)

```js
https://firestore.googleapis.com/v1/projects/{YOUR_PROJECT_ID}/databases/(default)/documents/{YOUR_COLLECTION}/{DOCUMENT_ID_YOU_WANT}
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

### 🚀 Update document (method : PUT (PATCH)) :

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

### 🚀 Delete document (method : DELETE) :

```js
https://firestore.googleapis.com/v1/projects/{YOUR_PROJECT_ID}/databases/(default)/documents/{YOUR_COLLECTION}/{DOCUMENT_ID}
```

</br>

# AUTHENTICATION 🔐

<br/>

### 🚀 Register (method : POST) :

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
 
 ### 🚀 Login (method : POST) :

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

### 🚀 Update email (method : POST) :

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

### 🚀 Update password (method : POST) :

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

### 🚀 Update account (method : POST) :

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

### 🚀 Delete user (method : DELETE) :

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

### 🚀 Get user info (method : POST) :

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

# STORAGE 📦

<br/>

### 🚀 Upload image (method : POST) :

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

### 🚀 Update image (method : POST) :

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

### 🚀 Delete image (method : DELETE) :

```js
https://firebasestorage.googleapis.com/v0/b/{projectID}.appspot.com/o/{folderName}%2F{pictureName}.png
```

<br/>

### 🚀 Get image info (method : GET) :

```js
https://firebasestorage.googleapis.com/v0/b/{projectID}.appspot.com/o/{folderName}%2F{pictureName}.png
```

<br/>

### 🚀 Image url :

```js
https://firebasestorage.googleapis.com/v0/b/{projectID}.appspot.com/o/{folderName}%2F{pictureName}.png?alt=media&token={imageDownloadToken}
```
