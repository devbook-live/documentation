## MVP:
1. User can type JS code into a text editor
2. User can run their code through a Node env and get results or error messages
3. User can share a given url so that other users can then edit the same doc
4. User can see a list of other users currently viewing / working on the same doc
5. Multiple users can work on the same document and see text changes in real time
6. Multiple users can coordinate and see results of a test in real time


### Next steps?:
- Login
- Ability to persist code after logging out
- Should have google docs-type “File” and “Edit” options
- Should look somewhat like google docs (material design)

### Possible advancements past MVP:
- User can log in with Google or Github
- Ability to add language-specific modules (expand build scripts)
- Support for other languages (and corresponding runtime envs)
“More of a Sandcastle” - DOM window, Postman-type results, Postico-type views
- Chat window so users can communicate
- Google drive-type views of docs
- Saving in real time (like google docs)
- Permissions - not necessarily everyone who has the link can edit


### Features/Stack:
##### Text editor:
- Firepad -> Firebase
- Possibly Postgres to store persisting docs
##### Code runner
- Docker
- Potentially develop and expand build scripts for multiple languages
- Potential for DOM, Postman-like and Postico-like capabilities (requiring, e.g., Docker container for DB)
##### Real time collaboration
- Firepad
##### Web app frame for everything else
- Express, React, Redux …
- Sequelize, Postgres for user info
- Google docs UI - Material UI



## What to start with
#### Text editor
- Research how Firepad and Firebase work together
How can we access what gets stored?
What does Firepad look like out of the box?
rich text toolbar and shortcuts enabled) ?
- Configure Firepad in app
Figure out how to make this real time - by default? Do we need to do anything?
- Research how to use Firepad features:
Cursor position synchronization,
Undo & redo,
Text highlighting,
User attribution,
Presence detection,
Version checkpointing,
https://firepad.io/
##### Short term goal: make it work. And make it work in real time for multiple users.

#### Code runner
What are the tasks to create a code-running container via Docker? Come up with a list of things we need to do...things like:
- Configure a Docker container…
What are the configuration files we need?
What settings, if any, do we care about? What defaults can we use?
Async stuff
- ...that runs Node
- And that is fault-tolerant
(Setting a time limit on how long code can run before timeout
And that is secure)
- How much of this comes out-of-the-box? Do we have to add anything?
##### Short term goal: plan out what we actually need to do. And make a container. Maybe, that can run Node

#### Web app container/frame for everything else
- List out Material UI components
- List out components
- Wireframe components, including behavior changes
- Route to get to a new page
- Page url includes firebase page id, so page can be shared
- If another user goes to that url, that should bring up what’s in firebase
- Eventually, persistent storage, login, etc.
#### Short term goal: make wireframes detailing components (including Material UI components - taking into account what Firepad gives us out of the box)
