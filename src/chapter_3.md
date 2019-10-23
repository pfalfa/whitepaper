# Core Technology

Pfalfa is developed using variety of existing open-source framework specialized in blockchain and decentralized peer to peer technology. We develop UI dashboard for developer to manage dApps from initializing new dApps, setting up connection to our database service (GunDB), storage service (IPFS) and optional smart contract deployment. We're utlizing [Embark CLI](https://embark.status.im/) by adding new plugin template specific for Pfalfa platform

## Embark CLI

[From their doc](https://embark.status.im/docs/overview.html)

Embark is a fast, easy to use, and powerful developer environment to build and deploy decentralized applications, also known as “DApps”. It integrates with Ethereum blockchains, decentralized storages like IPFS and Swarm, and decentralized communication platforms like Whisper.

Embark’s goal is to make building decentralized applications as easy as possible, by providing all the tools needed and staying extensible at the same time.

Some of Embark’s features, but not all of them, are:

* Automatic Smart Contract deployment - Embark takes care of deploying your Smart Contracts as well as redeploying them as you make changes to your code. 

* Client development - Build your application with the framework of your choice right within Embark.

* Testing - Test your applications and Smart Contracts through Web3 in JavaScript

* Decentralized app distribution - Embark integrates with decentralized storages like IPFS and helps you distributing your app in the network. 

* Peer-to-peer messaging - Send and receive messages via communication protocols like Whisper. 

* Cockpit - An companion application to make developing and debugging decentralized applications a breeze. 

## GunDB

[From their doc](https://gun.eco/docs/Introduction)

GUN is a small, easy, and fast data sync and storage system that runs everywhere JavaScript does. The aim of GUN is to let you focus on the data that needs to stored, loaded, and shared in your app without worrying about servers, network calls, databases, or tracking offline changes or concurrency conflicts.

## Ethereum

[From their doc](https://www.ethereum.org/beginners/)

Ethereum is the foundation for a new era of the internet:

* An internet where money and payments are built in.

* An internet where users can own their data, and your apps don’t spy and steal from you.
* An internet where everyone has access to an open financial system.
* An internet built on neutral, open-access infrastructure, controlled by no company or person.

Launched in 2015, Ethereum is the world’s leading programmable blockchain.

Like other blockchains, Ethereum has a native cryptocurrency called Ether (ETH). ETH is digital money. If you’ve heard of Bitcoin, ETH has many of the same features. It is purely digital, and can be sent to anyone anywhere in the world instantly. The supply of ETH isn’t controlled by any government or company - it is decentralized, and it is scarce. People all over the world use ETH to make payments, as a store of value, or as collateral.

## IPFS

[From their doc](https://docs.ipfs.io/introduction/)

IPFS stands for the InterPlanetary File System - a peer-to-peer network for storing and accessing files, websites, applications, and data in a distributed file system

## Ethereum Name Service

[From their doc](https://docs.ens.domains/)

ENS is the Ethereum Name Service, a distributed, open, and extensible naming system based on the Ethereum blockchain.

ENS’s job is to map human-readable names like ‘alice.eth’ to machine-readable identifiers such as Ethereum addresses, content hashes, and metadata. ENS also supports ‘reverse resolution’, making it possible to associate metadata such as canonical names or interface descriptions with Ethereum addresses.

ENS has similar goals to DNS, the Internet’s Domain Name Service, but has significantly different architecture, due to the capabilities and constraints provided by the Ethereum blockchain. Like DNS, ENS operates on a system of dot-separated hierarchical names called domains, with the owner of a domain having full control over subdomains.

## Developer Dashboard

Pfalfa provide dashboard for devleoper to manage theid dApps from web-based application, initiating new dApps, setting up database connection, IPFS gateway and setting up ENS domain based either using subdomain inside `pfalfa.eth` or using custom domain.