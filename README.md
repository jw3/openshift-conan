Conan Server for OpenShift
==========================

A Conan package manager server (`conan_server`) image for OpenShift

Artifacts are stored in `/var/lib/conan`

See the server conf for configuration details

### volumes

If running with Docker off of root, the volume will need to be either world writable or in the root group

For a new volume the easiest way is to

1. let docker create the volume dir
2. chmod the volume dir to 775
3. container will write to it

The default configuration expects the volume to be at `/var/lib/conan`, but this is not declared as a Docker volume to allow for committing the data dir if so desired.

### production use

The conan documentation advises against using `conan_server` in production

>The conan installer includes a simple executable conan_server for a server quick start. But you can use the conan server through the WSGI application, which means that you can use gunicorn to run the app, for example.

### see
- http://docs.conan.io/en/latest/uploading_packages/running_your_server.html
- https://docs.openshift.org/latest/creating_images/guidelines.html
