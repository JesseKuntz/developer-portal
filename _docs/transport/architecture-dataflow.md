---
title: Architecture Dataflow
subtitle:
tags: [transport, device, communicate, companion wallet]
category: Connect your app
author:
toc: true
layout: doc
---


## Dataflow Overview

During a transaction handled by Ledger Device several exchanges are done between different application & hardware components.
These exchanges allow to read data from Ledger Device & Sign Transactions with internal private key without sharing it.



{: .center}
[![Application Sequence Diagram](../images/application-sequence.png)](../images/application-sequence.png)
*Fig. 1: Application Sequence Diagram*


This diagram demonstrate the sequence of different calls done by each application layer during a transaction.
5 different layers are used to handle a transaction:

- **Your Application Core Code:** your software wallet
- **Ledger JS Transport API:** packages that allow you to implement several kind communication between the software wallet and a Ledger hardware wallet
- **Ledger JS Dedicated App Lib:** packages that allow you to communicate with specific Nano Apps
- **Nano App:** the application that run on a Ledger hardware wallet to interact with a specific blockchain
- **Ledger Device Software:** the operating system of Ledger harware devices

This workflow demonstrate a typical use case of Ledger Device using an Nano App Lib. If you are planning to integrate with a Nano API-less you have to complete all actions done by LedgerJS Dedicated App Lib within your application core code.
