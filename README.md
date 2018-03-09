# npm-free-registry
A registry implementation compatible with npm registry protocol.

This registry is born out of the idea to have a free and extensible registry which is compatible with the npm client. The registry is (will be) used as backend for the [Openscad-Module](https://github.com/RobertFach/Openscad-Modules) project.

The development of the registry is based on the following guidelines:
- seperation of application and backend (this is the main drawback of the [npm-registry-couchapp](https://github.com/RobertFach/npm-registry-couchapp) backend)
- extensibility and plugability (in the future, we want to try out microservice architectures)
- agile, test-driven development with continuous integration and continuous delivery
- Hyper-* (tm) :-)

## Registry API specification
- [API Spec. from NPM](https://github.com/RobertFach/registry/blob/master/docs/REGISTRY-API.md)

## Roadmap
* Implementation of [API Spec. from NPM](https://github.com/RobertFach/registry/blob/master/docs/REGISTRY-API.md) by reimplementing [npm-registry-couchapp](https://github.com/RobertFach/npm-registry-couchapp) backend
* Integrate services on backend side supporting [Openscad-Module](https://github.com/RobertFach/Openscad-Modules) project:
  - linting service for openscad-modules
  - namespace conflict warnings
  - semantic versioning checks (as far as possible)
  - more to be added...
