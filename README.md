# Exonum Blockchain Explorer

An application for monitoring blocks and transactions in Exonum blockchain.

![Exonum Blockchain Explorer](Screenshot.png)

First, install dependencies:

```sh
npm install
```

## Starting as a Node.JS server

Build sources:

```sh
npm run build
```

Run app:

```sh
npm start -- --port=3000 --api-root=http://127.0.0.1:8200
```

`--port` is a port for Node.JS app.

`--api-root` is a root URL of Exonum node public API.

## Build a static html pages

CORS headers must be setted up in Exonum node configuration to use the application as static html pages.
See `allow_origin` parameter in [Exonum docs](https://exonum.com/doc/architecture/configuration/#api).

Build sources:

```sh
npm run compile -- --env.apiRoot=http://127.0.0.1:8200
```

`--env.apiRoot` is a root URL of Exonum node public API.

Run [index.html](index.html).

## Use with outdated Exonum core

Explorer compatibility with Exonum core:

| Core version | Revision |
|---|---|
| unreleased | latest |
| 0.8+ | `d48fbad52b1a4ef39c65136e4caa1b725eacdb57` |
| 0.6+ | `f373661b8f780309fd3bfa2e351c21daa2a50d95` |
| 0.1+ | `467b651689d7d4fd369084948ef92a5b0fa11f2a` |

To use explorer with Exonum core 0.8 and below:

```sh
git checkout f373661b8f780309fd3bfa2e351c21daa2a50d95
```

## LICENSE

Exonum Blockchain Explorer is licensed under the Apache License (Version 2.0).
See [LICENSE](https://github.com/exonum/blockchain-explorer/blob/master/LICENSE) for details.
