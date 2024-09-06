<div align="center">
<h1>📄 FIREBASE RESTFUL API DOCS 📄</h1>
</div>


## DATABASE (Realtime) 🛢️

</br>

 ***Get list data (method : GET) :***

```js
https://{projectID}-default-rtdb.firebaseio.com/{listName}.json
```

</br>

***Delete list data (method : DELETE) :***

```js
https://{projectID}-default-rtdb.firebaseio.com/{listName}.json
```

</br>

 ***Post one data (method : POST) :***

```js
https://{projectID}-default-rtdb.firebaseio.com/{listName}.json
```

</br>

***Get, Update, Delete one data (methods : GET, PUT, DELETE) :***

```js
https://{projectID}-default-rtdb.firebaseio.com/{listName}/{dataID}.json
```

</br>

## DATABASE (Firestore) 🛢️

<br/>

## AUTH 🔐

***Register : (method : POST) :***

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

***Upload image (method : POST) :***

```js
https://firebasestorage.googleapis.com/v0/b/{projectID}.appspot.com/o/{folderName}%2F{pictureName}.png
```

<br/>

**Body**

```js
{file: {}}
```

<br/>

***Image url :***

```js
https://firebasestorage.googleapis.com/v0/b/{projectID}.appspot.com/o/{folderName}%2F{pictureName}.png?alt=media&token={imageDownloadToken}
```