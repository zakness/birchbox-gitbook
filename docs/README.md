---
description: Welcome to the Bernard Developer Documentation with Gitbook.
---

# Getting Started

## Development Environment Setup

Hey Curt

{% tabs %}
{% tab title="Local Setup" %}
### Environment Dependencies

* [Node.js](https://nodejs.org/en/download/) v6.6.0
* [yarn](https://yarnpkg.com/lang/en/docs/install/)

### Installation

Clone repo and install external dependencies:

```bash
git clone git@github.com:/birchbox/bernard_black && cd bernard_black
yarn
```

#### Running app server

```text
TARGET=[com|es|uk] yarn run start
```

Site now available at `localhost:3000` using staging backend.

#### Running app server with a built webpack bundle and hot reload turned off

```text
TARGET=[com|es|uk] yarn run start-bundle
```

Site now available at `localhost:3000` using staging backend.

#### Adding dependencies

```bash
yarn add ...
```

Consult yarn [docs](https://yarnpkg.com/en/docs/migrating-from-npm#toc-cli-commands-comparison) for specific options
{% endtab %}

{% tab title="Remote Setup" %}
On dev containers, Tech Ops has built a `node-app` CLI for managing the node server. The process is run in a separate environment, so you cannot run the `package.json` scripts directly like you can when developing locally.

Each target \(com, es, uk\) runs in a separate dev container.

#### App URL

```bash
https://app.USER.dev.birchbox.TLD
```

#### Repo location

```bash
cd ~/unit/TLD.birchbox.app/repo
```

#### Issue commands to node app

```bash
node-app -c [start, stop, restart, check]
```

Note that when the server is restarted, it takes up to a minute to rebuild the app and begin handling requests again.

#### Update or reinstall dependencies

```bash
node-app -c [update, reinstall]
```

`update` will run `npm install` and restart the server. `reinstall` does the same, but deletes the `node_modules` directory first.

#### Use staging APIs

By default the node app will use your dev container’s APIs. If you want to use staging instead, use the `API_ENV` environment variable:

```bash
API_ENV=staging node-app -c restart
```

#### Node server logs

```bash
cd ~/unit/TLD.birchbox.app/log/node-app
tail current
```
{% endtab %}
{% endtabs %}

