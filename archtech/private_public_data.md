# Private & Public Data

In QQuill, data is seperated into to major categories:
- private data
- public data

**Private data** is data which you're creating and generating yourself by using QQuill. You're essentially previewing certain QQuill animations.

**Public data** is published data, either by yourself, or by others, which can be accessed through the Akashic Lens.

Most of QQuill's workflow revolves around privately writing and engaging with your notes, concepts and ideas, gathering them in collections, and re-engaging with them over time. This involves linking concepts together, refining them by iterations, or even making them evolve through elemental energies.

Certain ideas might then want to get published, either for inspiration for others, or for collaborative features of QQuill. This involves publishing private data to a public domain.

When engaging with your private data, all data remains on device, and can be backed up in the cloud, either plain text, or encrypted (we recommend encrypting all your data). For this you may either choose to use QQuill's Backup Service, or Google Drive backups.

To enjoy synchronization, or gain access to any of QQuill's public services, authorization is required. There are three ways to create an account in QQuill:

1. Google Sign-In + Public Key Authentication
  - In this case, authentication happens via `JWT-tokens` provided by Google.
2. QQuill - Email + Public Key Authentication
  - In this case, authentication happens via a username and public key signature verification.

In both situations, a **private-public key** is required, and can either be imported or generated, which will empower you with military-level cryptographic powers, to keep private data which belongs to you, and allows our servers to ensure with 100% certainty, that data comes from you, and belongs to you.

We recommend you to store your **private-public keystring** (in settings > wallet > private keys) in a password manager of your choice, to ensure that you remain having access to your encrypted data, which might only get decrypted for a heavy price, once quantum decryption services become a thing.

## My QQuill

"My QQuill" is what you see when you open up QQuill. It includes the following data points (a complete list (todo_link_datamodels)[]):
- Things
  - Any post or element that the user is the author of, including metadata
  - Posts usually contain
    - Title
    - Markdown Content
    - Comment Section
    - Layouts
      - The layout contain saved layouts, which would include masonry-like layouts for [Collections, Things, Attachments], "pinned to a wall".
  - UX Description of thing display
    - Things usually come with a title, markdown, elements, display trees, and so much more.
    - They might also reveal 
- Collections
  - Title & About Section
  - List of Things
  - Layouts
    - Layouts contain information as to the layout withing a thing. The layout is a masonry-like form, which contains pinned elements to them.
    - All collection layout inherit the collection-layout-core, which is:
      - General Information Bar & Sigil
      - Feeds & Feed settings
        - Usually contain recommended planetary position systems.
        - Certain feeds might come from an Automated Intelligence System.
        - Most feeds come from statistics (usually computed models from memory) like likes, duration of interest, "similar of topic to", classification schemes, and more 
- Attachments
  - Any kind of universal-extension for playback, with a plugin system (via React WebComponents)
  - Captions
    - Captions to attachments are possible
  - Links
    - Links to notes
- Statistics & Precomputed Data Index
  - Speaking here of computed statistics for collections (elements, activity, average look-time since x days, look-time historical, etc)
  - Storage of mean-viewing time, historical-viewing-time
    - Users will be fed things which have lots of mean-viewing time, and are adequate to add at the n-th position, after other selected things, after-each-other in a feed, due to either experiment, or Q-Values in the table of the user.
  - 
- Synthesis ()
  - Lookup Index of Correspondence Corpae, Texts, Tutorials Keywords, and perhaps Program Prompts (PPs) for generation of more descriptions and texts.
  - Translations (usually based on c)
- Viewed QQuills
  - list of either community or public qquills, created by others.
  - Includes list of things like ids, public-keys, and more.
  - Includes an index of past viewed feeds, and interaction journeys.
- Courses
  - Any downloaded or subscribed courses, downloaded for offline use. Imported, or downloaded from QQuill Menu.
- Plugin List + Version
  - Contains a list of all configuration-modifiers, or user-based browser plugins, which allow one to experience QQuill from a whole other level. They usually "get sprinkled in according to desired settings" in the feeds and feed settings.
    - Eg: Reddit-Viewer
    - Eg: News-Viewer
    - Eg: Y-Viewer
    - Eg: V-Viewer (virtual reality plugins)


## Synergistic QQuill

The synergistic QQuill is a special version of My Quill, where a group of people receive a cryptographically signed consent to download new files from a possibly secret group of playground-makers.

## Public QQuill

The public QQuill is a public display, and is both a collaboration and a free-for-all, for its purpose is to explore other people's QQuills and distilled wisdom contained within, to generate Synergetistic QQuills for collaboration,as not to get mixed with other business-driven entertainment aspects.

## Lifecycle of a Thing, Collection, and Attachments










