$# npm-free-registry
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

## Development
### Getting started
1. First, you need to install [docker-ce](https://www.docker.com/community-edition) and [docker-compose](https://docs.docker.com/compose/)
2. Run the following command to start up the REST API:
```
$ docker-compose up
```
3. That's it. Now, you should be able to fire some requests against your local
running API under [`http://localhost:3000`](`http://localhost:3000`).

### Tests
* To run all test (e.g. unit and acceptance) use the following command:
```
$ docker-compose run --rm api npm run test
```
* If you only want to run a specific set of tests, use:
```
$ docker-compose run --rm api npm run test:<unit | acceptance>
```
