# Database Service

Traditional database systems are normally managed and maintained by single institutions which possess the supreme authorities over the whole database. This model is not fitting for data management between institutions where a mutual trust has not been really developed, which stands out particularly in the internet application environment.

Pfalfa database service has different approach, utilizing [GunDB](https://gun.eco/) which offer decentralized, peer-to-peer and offline first approach there is no single centralized server. Pfalfa will provide relay peers in multiple network one that may have more reliable resources than a browser.

## Technology

### What is Decentralized Database

> Decentralized databases means that no single server control the data, it sync across every node in this case, every user browser acted as peer node that sync each other automatically. 

And it means that all the data is distributed between the nodes of the network. If something is added, edited or deleted on any computer, it will be reflected in all the computers of the network. If there are some legal amendments accepted, new information will be spread among other users throughout the network. Otherwise, the data will be backed up to coincide with the other nodes. Thus, the system is self-sufficient and self-regulating. The databases are protected from deliberate attacks or accidental changes of information.

### Reliability, accessibility and data transfer rates

> Decentralized networks can withstand the significant pressure on the network.

All the nodes of the network have the data. So, the requests are distributed between the nodes. Therefore, the pressure doesn’t fall on one computer, but on all the network. In this case, the total capacity of the network is much larger than the centralized one has.

Since the number of computers in the decentralized or distributed network is large, DDoS attacks are possible only in case their capacity is much larger than that of the network. But that would be a very expensive attack. In a centralized model the response time is very in this case. Therefore, it can be considered that decentralized and distributed networks are safe.

The users might be located all over the world, and don't forget about possible Internet connection issues. In decentralized and distributed networks the client can choose the node and work with all required information.

### Scalability

> A centralized network cannot expand significantly.

In a centralized model, all the clients are connected to the server. Only the server stores all the data. Therefore, all requests about receiving, changing, adding or removing the data passes through the main computer. But the server resources are finite. Consequently, it is able to carry out its work effectively only for the specific number of participants. If the number of clients is larger, the server load may exceed the limit during the peak time. Decentralized and distributed models don't have this problem since the load is shared between several computers.

### Offline-First

When a browser peer asks for data, it'll merge the reply with its own data using a CRDT, then cache the result. This means that:

> The next time the browser asks for that data, the reply is instant, even when offline.
> Data is replicated on each browser that asked for it.
> If your server fails, you can still recover your data from the browsers.

This makes the loss of important information nearly impossible, as all copies of the data would need to be destroyed before it is lost.

## GunDB Implementation in Pfalfa Database Service

> Pfalfa platform provide dedicated GunDB master peer relay for each dApps. Each peer will be hosted in multiple cloud provider in multiple data center. Once dApps initiated from our Developer Dashboard, our GunDB Peer will automatically provisioning to serve dApps database requirement.