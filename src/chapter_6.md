# Storage Service

Pfalfa provide easy-to-use storage service for dApps on top of IPFS. Pfalfa also provide multiple IPFS gateway in multiple network which make it easy for developer to host dApps under IPFS distributed content.

## Technology

### What is Decentralized storage

> Decentralized storage means no single server acted as server, it's distributed equally using P2P technology accross every node. Instead of a central server, a peer to peer network is used to establish connections. Public key cryptography is built into the node addressing system and content addressing is used to index content. 

### Interplanetary File System (IPFS)

IPFS is a new system for storing data on a large number of computers. It is transport layer agnostic, meaning that it can communicate through transport layers like transmission control protocol (TCP), uTP, UDT, QUIC, TOR, and even Bluetooth) 

### Node addressing and connection security

* Nodes in the peer to peer network each hold private keys and release public keys, just like in Bitcoin or Ethereum.
* Node addresses are derived through hashing their public keys. Allowing connection verification through message signing.
* Their public keys can be used to encrypt data before it is transferred, preventing interception and theft.

Solutions to the security issues of today's web are built into this addressing system. There is no need for a trusted central certificate issuer to provide connection verification tools and all connections can easily be encrypted by default. No more SSL.

At its core, IPFS is a versioned file system that can take files and manage them and also store them somewhere and then tracks versions over time. IPFS also accounts for how those files move across the network so it is also a distributed file system.

IPFS has rules as to how data and content move around on the network that are similar in nature to bittorrent. This file system layer offers very interesting properties such as:

* websites that are completely distributed
* websites that have no origin server
* websites that can run entirely on client side browsers
* websites that do not have any servers to talk to

### HTTP VS IPFS

HTTP has a nice property where in the identifier is the location so it is easy to find the computers hosting the file and talk to them. This is useful and generally works very well but not in the offline case or in large distributed scenarios where you want to minimize load across the network.

In IPFS you separate the steps into two parts:

* Identify the file with content addressing
* Go and find it — when you have the hash then you ask the network you’re connected to 'who has this content? (hash)' and you connect to the corresponding nodes and download it.

The result is a peer to peer overlay that gives you very fast routing

### Content Addressing

A content address is derived by hashing a piece of content.

* That content address is then hashed again to derive a key name.
* The key name is associated with a human readable name in IPNS (IPFS’ address registry).

Instead of referring to objects (pictures, articles, videos) by which server they are stored on, IPFS refers to everything by the hash on the file. The idea is that if in your browser you want to access a particular page then IPFS will ask the entire network "does anyone have this file that corresponds to this hash?" and a node on IPFS that does can return the file allowing you to access it.

IPFS uses content addressing at the HTTP layer. This is the practice of saying instead of creating an identifier that addresses things by location, we're going to address it by some representation of the content itself. This means that the content is going to determine the address. The mechanism is to take a file, hash it cryptographically so you end up with a very small and secure representation of the file which ensures that someone can not just come up with another file that has the same hash and use that as the address. The address of a file in IPFS usually starts with a hash that identifies some root object and then a path walking down. Instead of a server, you are talking to a specific object and then you are looking at a path within that object.

In today's web, if a file is moved, all links to that file need to be updated if they are to resolve. Because IPFS addresses are derived from the content they refer to, if the content still exists anywhere on the network, links will always resolve. This removes any need for duplication of content, except for the purposes of greater persistence security or for scaling up serving capabilities.

## IPFS Implementation in Storage Service

> Pfalfa Platform will manage multiple IPFS gateway using IPFS cluster to maximize data redundancy anda availability to already decentralized storage accross IPFS. Using our CLI tool, developer can easily deploy dApps to our IPFS gateway which automatically pin and publish under IPNS. We also provide sub-domain to link between IPFS CID and your dApps domain. Please consult our Developer Documentation for more information.