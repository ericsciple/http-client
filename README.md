
<p align="center">
  <img src="actions.png">
</p>

# Actions Http-Client

[![Http Status](https://github.com/actions/http-client/workflows/http-tests/badge.svg)](https://github.com/actions/http-client/actions)

A lightweight HTTP client optimized for use with actions, TypeScript with generics and async await.

## Features

  - HTTP client with TypeScript generics and async/await/Promises
  - Typings included so no need to acquire separately (great for intellisense and no versioning drift)
  - [Proxy support](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/about-self-hosted-runners#using-a-proxy-server-with-self-hosted-runners) just works with actions and the runner
  - Targets ES2019 (runner runs actions with node 12+).  Only supported on node 12+.
  - Basic, Bearer and PAT Support out of the box.  Extensible handlers for others.
  - Redirects supported

## Install

```
npm install @actions/http-client --save
```

## Samples

See the [HTTP](./__tests__) tests for detailed examples.

## Errors

### HTTP

The HTTP client does not throw unless truly exceptional.

* A request that successfully executes resulting in a 404, 500 etc... will return a response object with a status code and a body.
* Redirects (3xx) will be followed by default.

See [HTTP tests](./__tests__) for detailed examples.

## Debugging

To enable detailed console logging of all HTTP requests and responses, set the NODE_DEBUG environment varible:

```
export NODE_DEBUG=http
```

## Node support

The http-client is built using the latest LTS version of Node 12. We also support the latest LTS for Node 6, 8 and Node 10.

## Contributing

We welcome PRs.  Please create an issue and if applicable, a design before proceeding with code.

once:

```bash
$ npm install
```

To build:

```bash
$ npm run build
```

To run all tests:
```bash
$ npm test
```
