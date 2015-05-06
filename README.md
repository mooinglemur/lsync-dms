# lsync-dms
Flexible web-based document management system

Phase I Features (all todo)
* POSIX object storage backend
* OpenStack Swift object storage backend (using tempurl for client accesses)
 * Container per authorized user in one account, or Swift account per authorized user
* SQLite metadata backend
* SQLite Full Text Search backend
* Object tracking (by content hash) to allow for arbitrary reorganizaion of objects
* Editable metadata is stored in object storage backend (Custom headers for Swift, xattrs for POSIX)
* All of the search/database backend stuff is re-generatable from the object stores
* Full text searching (FTS4 in sqlite)
* Tag searching
* Access control (public vs private) (and visibility) per object, including in search results

Phase II+ Features
* S3 object storage backend
 * Bucket per authorized user
* Multiple web frontends (for cloud storage backends)
* Synchronization of database updates for each web frontend via work queue, and ability to easily clone frontend database states or rebuild db from scratch on out-of-rotation frontend.
* Photo gallery
* Online (HTML5) Video gallery/with transcoding
* Exif data searching (geolocating photographs, search for photos within a given radius)
* Assigning geo metadata irrespective of exif (override)
