docker-zipkin
=============

This repository is based on two repos of OpenZipKin:

* [docker-zipkin](https://github.com/openzipkin/docker-zipkin)
* [docker-zipkin-dependencies](https://github.com/openzipkin/docker-zipkin-dependencies)

Since we need to deploy zipkin via Marathon, and the storage will be MySQL, so I remove the usage of docker-compose, and provide some environment variables need for enabling MySQL storage.
