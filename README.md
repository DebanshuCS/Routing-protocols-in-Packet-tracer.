
# Routing protocols in Packet tracer

Routing protocols help computer networks communicate effectively and efficiently. Regardless of network size, these protocols can help securely transfer data to its intended destination. Understanding the different types of routing protocols can help you determine which type is best to use.

Here, I have implemented the common routing protocol categorizations and explained the associated protocol types.

Once you know how to categorize routing protocols, you can learn more about different types.

1. Default Routing– 
This is the method where the router is configured to send all packets towards a single router (next hop). It doesn’t matter to which network the packet belongs, it is forwarded out to the router which is configured for default routing. It is generally used with stub routers. A stub router is a router that has only one route to reach all other networks. 

## Config Diagram

![ccoco-1](https://user-images.githubusercontent.com/118846871/211062954-c7e1a2f2-caaf-465c-941f-0d80eb3c69da.png)

Configuring default routing for R1: 

```bash
  R1(config)#ip route 0.0.0.0 0.0.0.0  172.16.10.5
```

Now configuring default routing for R2: 
```bash
  R2(config)#ip route 0.0.0.0 0.0.0.0  172.16.10.1
```


2. Routing information protocol (RIP)
RIP, an interior gateway protocol, is one of the first protocols created. You can use it with local area networks (LANs), which are linked computers in a small range, or wide area networks (WANs), which are telecommunications networks that cover a greater range. There are two different versions of this protocol type: RIPv1 and RIPv2.

RIPv1, the original version, is a classful protocol that examines and evaluates network paths based on the hops to the pre-determined destination. Typically, it communicates with other networks by broadcasting its IP address. Meanwhile, the newer version, RIPv2, shares its routing table through a multicast address, which identifies the main computer network. This version, which is a classless protocol, also features advanced security measures, like authentication, to protect data. RIPv2 is beneficial for smaller networks because it can only support router journeys of 15 hops or fewer.

Related: Types of Computer Servers and How They Function

3. Enhanced interior gateway routing protocol (EIGRP)
Cisco also developed EIGRP, which allows for 255 hops. This type classifies as a distance vector, interior gateway and classless protocol. It uses the reliable transport protocol and the diffusing update algorithm to speed up the data convergence process, which maximizes efficiency. When in use, a router can take information from other routers' tables and record them as references. If a change occurs, each router notifies its neighbor to help ensure they all know which data routes are in use. This helps prevent potential miscommunications between routers.

4. Open shortest path first (OSPF)
OSPF—which classifies as a link state, interior gateway and classless protocol—uses the shortest path first (SPF) algorithm to ensure the efficient transmission of data. Internally, this type maintains multiple databases with topology tables and information about its entire network. Typically, the information comes from link state advertisements sent by individual routers. The advertisements, which are like reports, share detailed descriptions of the path's distance and how many resources it may require.

OSPF uses an algorithm called Dijkstra to recalculate pathways when topology changes occur. It also uses authentication practices to ensure its data is secure throughout changes or network breaches. Small and large network organizations may benefit from using OSPF because of its scalability features.

5. Static routing – 
Static routing is a process in which we have to manually add routes to the routing table. 

Advantages for static routing– 
No routing overhead for router CPU which means a cheaper router can be used to do routing. 
It adds security because an only administrator can allow routing to particular networks only. 
No bandwidth usage between routers. 

Disadvantage for static routing– 
For a large network, it is a hectic task for administrators to manually add each route for the network in the routing table on each router. 
The administrator should have good knowledge of the topology. If a new administrator comes, then he has to manually add each route so he should have very good knowledge of the routes of the topology. 

