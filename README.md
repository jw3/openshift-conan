Conan Server for OpenShift
==========================

A Conan package manager server (`conan_server`) image for OpenShift

Artifacts are stored in `/var/lib/conan`

See the server conf for configuration details

### note

The conan documentation advises against using `conan_server` in production

>The conan installer includes a simple executable conan_server for a server quick start. But you can use the conan server through the WSGI application, which means that you can use gunicorn to run the app, for example.

### see
- http://docs.conan.io/en/latest/uploading_packages/running_your_server.html
- https://docs.openshift.org/latest/creating_images/guidelines.html
