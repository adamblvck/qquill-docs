# QQuill API

In this section QQuill API is documented, in particular its REST API, and nodejs libraries to communicate efficiently with the API.

## Cold Authentication

To maximise data ownership to users, all data communication happens in an encrypted fashion.

## REST API Calls

The REST API is made avaiblle at `https://api.qquill.app` through which all production services of QQuill go out in the world.

### POST `${QQUILL_API}/user/register` - Register user email for verification

To register a new user in QQuill, pass a long a POST request to `/user/register`, with the following minimum body:

```
{
	"email": 'example@test.com',
	"login_type": google or email
}
```

In both Google and Email logins, QQuill will be sending out a confirmation email with a short code which is required to be pasted into the app, to proceed further.

The verification email is sent from `noreply@qquill.blvckstudios.com`.

### POST `/user/verify` - Register user email for verification

This endpoint is to verify users, by passing the verification token sent to via email, by the user who wants to complete registratin and be allowed to send POST requests to `/user/verify`.

Send the following code to the following URL, to verify the user.

```

```

### POST `${QQUILL_API}/user/register` - Register user email for verification


### POST `${QQUILL_API}/data` - Store a blob in QQuill servers

The user is allowed to post a single thing, with a unique modification date. A synchronised object is unique defined by `user_public_key`,`data_id`,`data_store_key`,`data_last_mod_dt`, hence they can't be overwritten.

```javascript
	keypair = new themis.KeyPair();
	
	let privateKey = keypair.private().toString("base64");
	let publicKey = keypair.public().toString("base64");
	expect(publicKey).toBeTruthy();
	expect(publicKey).toBeTruthy();

	const thing = createThing("1234567890");
	const encrypted_thing = QAuth.themis_crypto.encrypt_obj(thing, privateKey, publicKey);

	console.log('encrypted thing', encrypted_thing)

	// compose object for posting to the store
	const data_object = {
		public_key: publicKey,
		data_blob: encrypted_thing, // base 64, up to 100Mb
		data_id: thing.id,
		data_store_key: 'things/test',
		data_last_mod_dt: thing?.modified_dt?.toString().replace(/"/g, ''),
		data_scope: 'private', // private, or in publication channel_id (like a chat room or subreddit)
		data_is_encrypted: true, // if false, then data_blob is not encrypted
		data_meta: {
			filetype:'png' // relevant for qquill app, can be anything that I like, and the metadata in general can be anything that I like
		}
	};

	await sleep(100);

	const signed_json = QAuth.themis_crypto.sign_json(data_object, privateKey);
	console.log(signed_json);
	expect(signed_json).toBeTruthy();
	const verified = QAuth.themis_crypto.verify_json(JSON.parse(signed_json), publicKey);
	expect(verified).toBeTruthy();
	console.log(verified);

	await sleep(100);

	// Testing local API
	const myHeaders = {
		"x-qquill-pub": public_key,
		"Content-Type": "application/json"
	}

	const requestOptions = {
		method: "POST",
		headers: myHeaders,
		body: body,
		redirect: "follow"
	};

	const results = await fetch(`http://localhost:3003${endpoint}`, requestOptions)

	return await results.json();
```

### Deletion of user data

In QQuill, when data is deleted, it is moved to a trash folder, and deleted after a 30 days period. When syncing with QQuill, we register the deletion of data, and on other devices, the data is also deleted (aka moved into the Trash folder).

Our QQuill servers will daily sweep and check user data, is any is older than 30 days, the things are deleted from our servers, including your encrypted backups.
You can also manually delete data for a particular thing - by visting the data management screen, then deleting the data fully and completely. This then sends a POST request to `${QQUILL_AOUI}/data/delete` endpoint.

On QQuill as well (the app), each startup will launch a background process to check if any data is pending deletion, and if so, it will be deleted permantently from the app as well. You can explore the current status of stored data in the data management screen.



### 

## Cloud Deployment



### Local Development



### Deploying to QQuill

