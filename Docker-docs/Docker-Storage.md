# Docker Storage management

**Docker uses storage drivers to store Image layers and store data in the writable layer of a container. The Container layer does not persist after the container is deleted, but it is suitable for storing ephemeral data that is generated at runtime.**

Docker supports the following types of storage mounts for storing data outside of the writable layer of the container:

Volume mounts

Bind mounts

tmpfs mounts

Named pipes
