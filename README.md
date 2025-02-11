This repository demonstrates a common error in Dockerfiles: using the `latest` tag for base images. This can lead to inconsistencies in the build process, as the base image can change unexpectedly.

The `Dockerfile` shows the buggy code; the `Dockerfile-fixed` provides the solution.

**Problem:** The `latest` tag in `FROM ubuntu:latest` is not specific enough.  Future builds might use a different ubuntu version, leading to build failures or unexpected behavior. 

**Solution:** Specify a specific version of ubuntu, e.g., `FROM ubuntu:20.04`, to ensure consistent builds.