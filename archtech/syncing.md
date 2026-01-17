## QQuill Data Syncing

All data within QQuill can be synced.

## Private Data Syncing

Private data is synced through incremental steps, and checkpoints.

Data is usually synced once per post update, with the latest post coming first.
There are also full-checkpoint syncs, upon which the incremental updates are pushed to.

In this sense, we have
- thing/collection update:
  - new full json to use
  - modification date
  - link to checkpoint which this one requires
- checkpoint update
	- bulk.json
	- either encrypted, or plain things
	- contains all changes from-to a certain date
	- Checkpoints are-bulk containers of LAST MODIFIED STATE FOR EACH THING, from a certain modified data, to a certain modified date.
    	- The QQuill service automatically bundles things together on their last modifed things


### Uploading




### Themis Encryption

#### Nodejs / Lambda security

All of the websyncing and AI services are executed using powerful and juicy nodejs. For encryption we use Themis.

To make themis work for local development, run the following:

```bash
brew tap cossacklabs/tap
brew install libthemis

```


## Publishing Public Data



