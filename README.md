<p align="center">
  <img src="https://firebase.google.com/static/downloads/brand-guidelines/SVG/logo-standard.svg" />
</p>
<p align="center">
  <img src="https://cdn2.hubspot.net/hubfs/439485/Official_Logos/RESTful-API-logo-for-light-bg.png#keepProtocol" width="50%" />
</p>


</br>

## DATABASE 🛢️ (Realtime)

</br>

**_Get list data (method : GET) :_**

```js
https://{projectID}-default-rtdb.firebaseio.com/{listName}.json
```

</br>

**_Delete list data (method : DELETE) :_**

```js
https://{projectID}-default-rtdb.firebaseio.com/{listName}.json
```

</br>

**_Post one data (method : POST) :_**

```js
https://{projectID}-default-rtdb.firebaseio.com/{listName}.json
```

</br>

**_Get, Update, Delete one data (methods : GET, PUT, DELETE) :_**

```js
https://{projectID}-default-rtdb.firebaseio.com/{listName}/{dataID}.json
```

<br/>

## DATABASE 🛢️ (Firestore)

<br/>

**_Get all documents (method : GET) :_**

```js
https://firestore.googleapis.com/v1/projects/{YOUR_PROJECT_ID}/databases/(default)/documents/{YOUR_COLLECTION}
```

</br>

**_Get document (method : GET) :_**

```js
https://firestore.googleapis.com/v1/projects/{YOUR_PROJECT_ID}/databases/(default)/documents/{YOUR_COLLECTION}/{DOCUMENT_ID}
```

</br>

**_Post document (method : POST, random id) :_**

```js
https://firestore.googleapis.com/v1/projects/{YOUR_PROJECT_ID}/databases/(default)/documents/{YOUR_COLLECTION}
```

</br>

**Body**

```js
{
  "fields": {
    "email": {
      "stringValue": "test@example.com"
    },
    "password": {
      "stringValue": "test123"
    }
  }
}
```

<br/>

**_Post document (method : POST (PATCH), create a document with the name you want)_**

```js
https://firestore.googleapis.com/v1/projects/{YOUR_PROJECT_ID}/databases/(default)/documents/{YOUR_COLLECTION}/{DOCUMENT_ID}
```

</br>

**Body**

```js
{
  "fields": {
    "email": {
      "stringValue": "test@example.com"
    },
    "password": {
      "stringValue": "test123"
    }
  }
}
```

</br>

**_Update document (method : PUT (PATCH)) :_**

```js
https://firestore.googleapis.com/v1/projects/{YOUR_PROJECT_ID}/databases/(default)/documents/{YOUR_COLLECTION}/{DOCUMENT_ID}
```

</br>

**Body**

```js
{
  "fields": {
    "email": {
      "stringValue": "test@example.com"
    },
    "password": {
      "stringValue": "test123"
    }
  }
}
```

</br>

**_Delete document (method : DELETE) :_**

```js
https://firestore.googleapis.com/v1/projects/{YOUR_PROJECT_ID}/databases/(default)/documents/{YOUR_COLLECTION}/{DOCUMENT_ID}
```

</br>

## AUTH 🔐

<br/>

**_Register : (method : POST) :_**

```js
https://identitytoolkit.googleapis.com/v1/accounts:signUp?key=[API_KEY]
```

<br/>

**Body**

```js
{"email": "xxxx@gmail.com", "password": "xxxxxxxx", "displayName" : "xxxx", "returnSecureToken" : true}
```

</br>
 
 ***Login : (method : POST) :***

```js
https://identitytoolkit.googleapis.com/v1/accounts:signInWithPassword?key=[API_KEY]
```

</br>

**Body**

```js
{"email": "xxxx@gmail.com", "password": "xxxxxxxx", "returnSecureToken" : true}
```

</br>

## STORAGE 💾

<br/>

**_Upload image (method : POST) :_**

```js
https://firebasestorage.googleapis.com/v0/b/{projectID}.appspot.com/o/{folderName}%2F{pictureName}.png
```

<br/>

**Body**

```js
{file: {}}
```

<br/>

**_Image url :_**

```js
https://firebasestorage.googleapis.com/v0/b/{projectID}.appspot.com/o/{folderName}%2F{pictureName}.png?alt=media&token={imageDownloadToken}
```