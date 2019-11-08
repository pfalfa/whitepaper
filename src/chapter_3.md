# Core Technology

Pfalfa is developed using variety of existing open-source framework specialized in blockchain and decentralized peer to peer technology. We develop UI dashboard for developer to manage dApps from initializing new dApps, setting up connection to our database service (GunDB) and storage service (IPFS) as well.

Backed by Pfalfa Token built on top of Parity Substrate Framework allow us to have decentralized asset exchange marketplace for both developer and end-user

### GunDB

![GunDB](https://camo.githubusercontent.com/36a3253e47dad84b51c325ef5c2b532916a016e1/68747470733a2f2f636c6475702e636f6d2f5445793979476834356c2e737667 "GunDB Logo")

[From their doc](https://gun.eco/docs/Introduction)

GUN is a small, easy, and fast data sync and storage system that runs everywhere JavaScript does. The aim of GUN is to let you focus on the data that needs to stored, loaded, and shared in your app without worrying about servers, network calls, databases, or tracking offline changes or concurrency conflicts.

GUN is fully decentralized (peer-to-peer or multi-master), meaning that changes are not controlled by a centralized server. A server can be just another peer in the network, one that may have more reliable resources than a browser. You save data on one machine, and it will sync it to other peers without needing a complex consensus protocol. It just works.

### IPFS

[From their doc](https://docs.ipfs.io/introduction/)

![IPFS](https://steemitimages.com/p/5ShzsKnKF7vqAUfn3oKdyUKZJrgk43A2Ca64gND96PuSQjo8U4hZ6ZGwHJQDBhUeBGK1zsaYUdGaXK1AnQZnU6nKCvT8L8yVxVxbAHFQas8kvYycRQeyRqkgY5wLpBrbLD61eFcvuuC5V544gKA82wRg?format=match&mode=fit "IPFS Logo")



IPFS stands for the InterPlanetary File System - a peer-to-peer network for storing and accessing files, websites, applications, and data in a distributed file system

### Parity Substrate

[From their doc](https://substrate.dev/docs/en/overview/)

![Substrate](https://s3.amazonaws.com/media-p.slid.es/uploads/351278/images/5425886/logo-parity-substrate-4.svg "Substrate Logo")

Substrate is a blockchain platform with a completely generic State Transition Function (STF) and modular components for consensus, networking, and configuration.

Despite being "completely generic", it comes with both standards and conventions - particularly with the Substrate Runtime Module Library (SRML) - regarding the underlying data-structures that power the STF, thereby making rapid blockchain development a reality.

## Pfalfa Platform 

Pfalfa consist of both Developer Dashboard where developer manage their own dApps and dApps Store where end user can browse any dApps inside Pfalfa Platform.

### Developer Dashboard

Once developer register and login, they can start initiate new dApps, connect to our database relay peer and start deploying dApps intou our IPFS Gateway using provided CLI Tools. Each dApps will have it's own relay peer hence not interfere with other dApps.

### dApps Store

Once dApps published, it will automatically available for user to browse and use the dApps, optionally it can be integrate with our Identity Hub or doing transaction inside dApps using Pfalfa Gold token. There will be small transaction for each transaction occured in the platform. 