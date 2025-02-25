# Docker Storage management

**Docker uses storage drivers to store Image layers and store data in the writable layer of a container. The Container layer does not persist after the container is deleted, but it is suitable for storing ephemeral data that is generated at runtime.**

Docker supports the following types of storage mounts for storing data outside of the writable layer of the container:

Volume mounts

Bind mounts

tmpfs mounts

Named pipes

### There two main ways to manage data persistence and share files between containers and the host system:
**Feature of Volumes:**
- **Location:**	Stored in Docker-managed directories (/var/lib/docker/volumes/)
- **Security:**	More secure Docker manages it.
- **Use Case:**	Databases, persistent app data

**Feature of Bind Mounts**

- **Location:** Any location on the host filesystem
- **Security:** Less secure due to direct access to host filesystem
- **Use Case:** Sharing config files, local development
