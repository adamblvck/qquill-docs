## Syncing Setup

QQuill is primarily a life planning and understanding tool, which requires all data to be locally stored and managed, where any data backups are to be stored in either an encrypted or decrypted fashion.

Secondly, it helps to get inspired by joining certain publications for inspiration, which is the public part of QQuill: users are empowered to publish their best notes and ideas, either to their QQuill Public, private platforms (dropbox / gdrive), or social media platforms.

The main goal of the syncing setup of QQuill, is to give people several options to synchronise their private data.

QQuill Public primarily synchronises any published content to a publication channel on QQuill, which allows other users to engage with community content using the four element framework. 

For even more advanced proofing of one's creation, QQuill would allow people to time-brand their content for 500-year permanent timestamp seals, with no government or army required! The same content can also be converted to an NFT for $1 per publication, for an untemperable timestamp-brand for a concept, attachment, idea, or write-up, and thus will also remain registered for the coming 500 years into the future. The QQuill Smart Contracts can either be published to QQuill Public Smart Contract, or your personal NFT contract be transfered to one of your personal accounts, if you'd need to do so.

## Cloud Setup for QQuill Syncing & Public

- RDS: PostgreSQL DB for storaging registered users, sync-service cache, AI usage, and any anymous app analytics.
- API Access with Lambda Integration: for access to QQuill Services in a secure way.
- VPC Configuration: a secure place in the cloud where only VPNs and API authorization allows modification of data in the database.
- Individual Vector Databases: a per-person vector search database (docker?), allowing people to privately and deeply engage with AI. Engaging with the docker can only happen through an API within the instance, which can only be accessed through signed messages by the user's private key.

One thing that now came up, is setting up pg_hba.conf, to allow proper connection from the Lambda to the RDS.

## The Cloud Setup

We have a postgresql instance, to register users, their purchases, and any potential "permalinks" to previous states of their journal. Even if these permalinks would be stored in a local environment, the general setup is that the postgres-instance helps to index the synchronization space of the user, which is basically like a gdrive in the cloud. Either use "our cloud storage" or your own storage, you'll still be required to go through a type of caching service.

SpellBook/QQuill is a manager to this underlying data, but they can always be exported to other representations, like Markdown files, PDFs, CSVs, and more. The stored data within the permalinks are then downloaded for local first usage, and neatly and thoroughly organised and displayed in a feed / editor / ideation thing.

The postgresql instance has the following tables:

- 







