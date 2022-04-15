---
title: Boilerplate plugin
subtitle:
tags: [dapp, DApp plugin]
category: "Live App: Dapp integration"
author:
toc: true
layout: doc
---

Here is a boilerplate plugin to help you write your own. This guide walks you through the plugin.

You can follow it best by forking the repository [https://github.com/LedgerHQ/app-plugin-boilerplate](https://github.com/LedgerHQ/app-plugin-boilerplate) in the `plugin_dev/` folder:

```sh
cd ..
git clone https://github.com/LedgerHQ/app-plugin-boilerplate
```

We will need the Ethereum SDK to build our plugin. It can be cloned anywhere, but it is easier to add it directly inside the `app-plugin-boilerplate` directory:

```sh
cd app-plugin-boilerplate/
git clone https://github.com/LedgerHQ/ethereum-plugin-sdk
```

<!--  -->
{% include alert.html style="important" text="The SDk repository defaults on branch \"master\", which is synchronized with the Ethereum application latest stable version.

If your want to work on a newer but unstable version, checkout the \"develop\" branch.
" %}
<!--  -->

## What's what

There is no need to build it right now, only after adding tests. For now, in `app-plugin-boilerplate/` there are these folders:
- `ethereum-plugin-sdk`: This repository contains information shared by the Ethereum app and your plugin, such as structure definitions, utility functions, etc.
- `icons`: plugin icons as displayed on the device. We will get to it later, but you can read about it [here](https://developers.ledger.com/docs/nano-app/design-requirements/).
- `src`: the actual source code (in C).
- `tests/`: the test folder (using the js Testing Framework).

## Change plugin name

There is the `Makefile` directly in the repository root. 
You need to open `Makefile` and change `APPNAME` to suit your plugin name (e.g., `Paraswap`, `1inch`, `Lido`, etc.).
