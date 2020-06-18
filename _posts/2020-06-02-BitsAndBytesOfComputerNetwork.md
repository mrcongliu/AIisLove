---

layout: post

description: The Second Section of Coursera IT support Specialist.

categories: [Computer Science]

title: The Bits and Bytes of Computer Networking

---



Key Concepts**

- Describe how the TCP/IP five layer network model works.
- Identify basic networking devices.
- Label each of the five layers in the TCP/IP network model.
- Describe how the physical layer works.
- Describe how the data link layer works.



> The Start of Week 1
>
> ---



### 1. The TCP/IP Five-Layer Network Model

![]({{ site.baseurl }}/images/layers.JPG "The TCP/IP Five-Layer Network Model")



#### 1.1 Physical Layer

Represents the physical devices that interconnect computers



#### 1.2 Data Link Layer

Responsible for defining a common way of interpreting these signals so network devices can communicate

> The **Ethernet** standards also define a protocol responsible for getting data to nodes on the same network or link.



#### 1.3 Network Layer

Allows different networks to communicate with each other through devices known as routers

> **Internetwork**
>
> A collection of networks connected together through routers, the most famous of these being the **Internet**

> **IP(Internet Protocol)**
>
> IP is the heart of the Internet and most small networks around the world.



#### 1.4 Transport Layer

Sorts out which client and server programs are supposed to get that data

> **TCP(Transmission Control Protocol)**
>
> **UDP(User Datagram Protocol)**
>
> The big difference between the two is that TCP provides mechanisms to ensure that data is reliably delivered while UDP does not.



#### 1.5 Application Layer

The protocols at play in the application layer will be most familiar to you, since they are the ones you probably interacted with directly before, even if you didn't realize it.



 

> You can think of layers like different aspects of a package being delivered. 
>
> 1. The physical layer is the delivery truck and the roads. 
>
> 2. The data link layer is how the delivery trucks get from one intersection to the next over and over. 
>
> 3. The network layer identifies which roads need to be taken to get from address A to address B. 
>
> 4. The transport layer ensures that delivery driver knows how to knock on your door to tell you your package has arrived. 
>
> 5. The application layer is the contents of the package itself.

![]({{ site.baseurl }}/images/animationOfLayers.JPG "Animation of Layers")



#### 1.6 Supplementary Reading for The OSI Networking Model

In addition to the five layer model, it's importance to note that other models exist. For example, the **traditional TCP/IP Model** only has four layers, as it doesn't differentiate between the physical layer and the data link layer. The most well know other model is the **OSI model**.

The primary difference between our five layer model and the seven layer OSI model is that the OSI model abstracts the application layer into three layers total.

Learn more about the OSI Networking Model:

- [**https://www.sans.org/reading-room/whitepapers/standards/osi-model-overview-543**](https://www.sans.org/reading-room/whitepapers/standards/osi-model-overview-543)
- [**https://en.wikipedia.org/wiki/OSI_model**](https://en.wikipedia.org/wiki/OSI_model)



### 2. The Basics of Networking Devices

#### 2.1 Cables

Connect different devices to each other, allowing data to be transmitted over them

> Most network cables used today can be split into two categories: 
>
> * Copper (the most common form)
> * Fiber (Fiber Optic Cables)

The most common forms of copper twisted-pair cables used in networking are Cat5, Cat5e, and Cat6 cables.

Differences in how these twisted pairs are arranged inside these cables can drastically alter how quickly data can be sent accross them and how resistent these signals are to outside interference.

Cat5e cables have mostly replaced those older Cat5 cables because their internals reduce crosstalk.

> **Crosstalk**
>
> When an electrical pulse on one wire is accidentally detected on another wire

Cat6 cables follow an even more strict specification to avoid crosstalk, making those cables more expensive. Cat6 cables can transfer data faster and more reliably than Cat5e cables can, but because their internal arrangement, they have a shorter maximium distance when used at higher speeds.

> **Fiber Cables**
>
> Contain individual optical fibers, which are tiny tubes made out of glass about the width of a human hair

Unlike copper, which uses electrical voltages, fiber cables use pulses of light to represent the ones and zeros of the underlying data.

Fiber is even sometimes used specifically in environments where there's a lot of electromagnetic interference from outside sources. Because this can impact data being sent across copper wires.

Fiber cables can generally transport data quicker than copper cables can, but they're much more expensive and fragile. Fiber can also transport data over much longer distances than copper can without suffering potential data loss.



#### 2.2 Hubs and Switches

Unlike cables, which allow you to form point-to-point networking connections, there are network devices that allow for many computers to communicate with each other. The most simple of these devices is a hub.

> **Hub**
>
> A physical layer device that allows for connections from many computers at once.

![]({{ site.baseurl }}/images/hub.jpg "Hub")

All devices connected to a hub will end up talking to all other devices at the same time. It's up to each system connected to the hub to determine if the incoming data was meant for them, or to ignore it if it isn't. These causes a lot of noise on the network and creates what's called a collision domain.

> **Collision Domain**
>
> A network segment where only one device can communicate at a time.
>
> If multiple systems try sending data at the same time, the electrical pulses sent across the cable can interfere with each other.

These slows down network communications, and is the primary reason hubs are fairly rare. They're mostly a historical artifact today. A much more common way of connecting many computers is with a more sophisticated device, known as a network switch, originally known as a switching hub. 

![]({{ site.baseurl }}/images/switch.png "Switch")

A switch is very similar to a hub, since you can connect many devices to it so they can communicate. The difference is that while a hub is a layer 1 or physical layer device, a switch is a level 2 or data link device. 

![]({{ site.baseurl }}/images/hub&switch.png "hub vs switch")

This means that a switch can actually inspect the contents of the Ethernet protocol data being sent around the network, determine which system the data is intended for and then only send that data to that one system. This reduces or even completely eliminates the size of collision domains on a network.



#### 2.3 Routers

> **Hubs and switches**
>
> The primary devices used to connect computers on a single network, usually referred to as a **LAN**, or **local area network**

> **Router**
>
> A device that knows how to forward data between independent networks

While a hub is a layer 1 device and a switch is a layer 2 device. A router operates at layer 3, a network layer.

![]({{ site.baseurl }}/images/router.png "router operates at layer 3")

Just like a switch can inspect Ethernet data to determine where to send things, a router can inspect IP data to determine where to send things.

![]({{ site.baseurl }}/images/router inspect IP data.png "router can inspect IP data")

Routers store internal tables containing information about how to route traffic between lots of different networks all over the world. The most common type of router you'll see is one for a home network, or a small office. These devices generally don't have very detailed routing tables. The purpose of these routes is mainly just to take traffic originating from inside the home, or office LAN, and to forward it along to the ISP, or Internet Service Provider. Once traffic is at the ISP, a way more sophisticated type of router takes over. These core routers from the backbone of the Internet and are directly responsible for how we send and receive data all over the Internet every single day. Core ISP routers don't just handle a lot more traffic than a home or a small office router. They also have to deal with much more complexity in making decision about where to send traffic. 

![]({{ site.baseurl }}/images/routerTraffic.png "router's traffic")

A core router usually has many different connections to many other routers. Routers share data with each other via a protocol known as BGP, or Border Gateway Protocol.

> **Border Gateway Protocol**
>
> Routers share data with each other via this protocol, which lets them learn about the most optimal paths to forward traffic

When you open a web browser and load a webpage, the traffic between computers and the web servers could have traveled over dozens of different routers. The Internet is incredibly large and complicated. And routers are global guides for getting traffic to the right places.



#### 2.4 Servers and Clients

The simplest way to think of server is as something that provides data to something requesting that data. The thing receiving the data is referred to as a client.

A server is anything that can provide data to a client, but we can also use the word to refer to the primary purpose of various nodes on our network.

![]({{ site.baseurl }}/images/server&client.png "server vs client")



### 3. The Physical Layer

#### 3.1 Moving Bits Across the Wire

In some ways, the physical layer of our network stack model is the most complexible. Its main focus is on moving ones and zeros from one end of the link to the next. The physical layer consists of devices and means of transmitting bit across computer networks.

> **Bit**
>
> The smallest representation of data that a computer can understand; it's a one or a zero

These ones and zeros send across networks at the lowest level are what make up the frames and packets of data. The takeaway is that it doesn't matter whether you're streaming your favorite song, emailing your boss, or using an ATM, what you're really doing is sending ones and zeros across the physical layer of the many different networks between you and the server you're interacting with.

A standard copper network table, once connected to devices on both ends, will carry a constant electrical charge. Ones and zeros are sent across those network cables through a process called modulation.

> **Modulation**
>
> A way of varying the voltage of this charge moving across the cable

When used for computer networks, this kind of modulation is more specifically known as line coding. It allows devices on either end of a link to understand that an electrical charge in a certain state is a zero, and in another state is a one. Through this seemingly simple techniques, modern networks are capable of moving 10 billion ones and zeros across a single network cable every second.

![]({{ site.baseurl }}/images/lineCoding.png "line coding")



#### 3.2 Twisted Pair Cabling and Duplexing

The most common type of cabling used for connecting computing devices is known as twisted pair. It's called a twisted pair cable because it features pairs of copper wires that are twisted together. These pairs act as a single conduit for information, and their twisted nature helps protect against electromagnetic interference and crosstalk from neighboring pairs.

![]({{ site.baseurl }}/images/cablePairs.png "cable pairs")

A standard Cat6 cable has eight wires consisting of four twisted pairs inside a single jacket. Exactly how many pairs are actually in use depends on the transmission technology being used. But in all modern forms of networking, it's important to know that these cables allow for duplex communication.

> **Duplex communication**
>
> The concept that information can flow in both directions across the cable

>  **Simplex communication**
>
> This process is unidirectional

Think about a baby monitor, where the transmission of data only goes in one direction making it a simplex communication. A phone call on the other hand is duplex since both parties can listen and speak. 

![]({{ site.baseurl }}/images/duplex.png "Simplex vs Full-duplex")

The way networking cables ensure that duplex communication is possible is by reserving one or two pairs for communication in one direction. They then use other one or two pairs for communicating in the other direction. So, devices on either side of a networking link can both communicate with each other at the exact same time. This is known as full duplex. 

![]({{ site.baseurl }}/images/half-duplex.png "Half-duplex")

If there's something wrong with the connection, you might see a network link degrade and report itself as operating as half-duplex. Half-duplex means that, while communication is possible in each direction, only one device can be communicating at a time.



#### 3.3 Supplemental Reading for Ethernet Over Twisted Pair Technologies

**Ethernet over twisted pair technologies** are the communications protocols that determine how much data can be sent over a twisted pair cable, how quickly that data can be sent, and how long a network cable can be before the data quality begins to degrade.

Read more about Ethernet over Twisted Pair technologies:

https://en.wikipedia.org/wiki/Ethernet_over_twisted_pair



#### 3.4 Network Ports and Patch Panels

The final steps of how the physical layer works take place at the end points of our network links. Twisted Pair network cables are terminated with a plug that takes the individual internal wires and exposes them. The most common plug is knows as an RJ-45 or Registered Jack 45. 

![]({{ site.baseurl }}/images/RJ45-plug.png "RJ45 port and plug")

It's one of many cable plugs specifications but by far the most common in computer networking. A network cable with an RJ-45 plug can connect to an RJ-45 network port.

> **Network ports** are generally directly attached to the devices that make up a computer network.

Switches would have many network ports because their purpose is to connect many devices. But servers and desktops usually only have one or two. Your laptop, tablet or phone probably don't have any.

![]({{ site.baseurl }}/images/linkLight.png "Link light vs activity light")

Most network ports have two small LEDs. One is the link light and the other is the activity light. The link light will be lit when a cable is properly connected to two devices that are both powered on. The activity light will flash when data is actively transmitted across the cable. A long time ago, the flashing in the activity light corresponded directly to the one's and zero's being sent. Today, computer networks are so fast that the activity light doesn't really communicate much other than if there's any traffic or not. On switches, sometimes the same LED is used for both link and activity status. It might even indicate other things like links speed. You'll have to read up on a particular piece of hardware you're working with but there will almost always be some troubleshooting data available to you through port lights. Sometimes a network port isn't connected directly to a device. Instead, there might be network ports mounted in a wall or underneath your desk. These ports are generally connected to the network via cables ran through the walls that eventually end at a patch panel.

![]({{ site.baseurl }}/images/patchPanel.png "Patch panel")

A patch panel is a device containing many net ports but it does no other work. It's just a container for the endpoints of many runs of cable. Additional cables are then generally ran from a patch panel to switches or routers to provide network access to the computers at the other end of those links.



### 4. The Data Link Layer

#### 4.1 Ethernet and MAC Addresses

It is quite surprising to know that traditional cable networks are still the most common option in the workplace and definitely in the data center. The protocol most widely used to send data across individual links is known as Ethernet. Ethernet and the data link layer provide a means for software at higher levels of the stack to send and receive data. One of the primary purposes of this layer is to essentially abstract away the need for any other layer to care about the physical layer and what hardware is in use. By dumping this responsibility on the data link layer, the Internet, transport and application layers can all operate the same no matter how the device they're running on is connected. So, for example, your web browser doesn't need to know if it's running on a device connected via a twisted pair or a wireless connection. It just needs the underlying layers to send and receive data for it. 

![]({{ site.baseurl }}/images/dumping.png "Data link layer")

Key concepts of this section:

* What MAC addresses are and how they're used to identify computers.
* The various components that make up an Ethernet frame.
* Differences between Unicast, Multicast and Broadcast addresses.
* How cyclical redundancy checks help ensure the integrity of data sent via Ethernet.

Ethernet is a fairly old technology. It first came into being in 1980 and saw its first fully polished standardization in 1983. Since then, a few changes have been introduced primarily in order to support ever-increasing bandwidth needs. For the most part though, the Ethernet in use today is comparable to the Ethernet standards as first published all those years ago. 

In 1983, computer networking was totally different than it is today. One of the notable differences in land topology was that the switch or switchable hub hadn't been invented yet. This meant that frequently, many or all devices on a network shared a single collision domain. You might remember from our discussion about hubs and switches that a collision domain is a network segment where only one device can speak at a time. This is because all data in a collision domain is sent to all the notes connected to it. If two computers were to send data across the wire at the same time, this would result in literal collisions of the electrical current representing our ones and zeros, leaving the end result unintelligible. Ethernet, as a protocol, solved this problem by using a technique known as **Carrier Sense Multiple Access with Collision Detection**(CSMA/CD).

> **CSMA/CD**
>
> Used to determine when the communications channels are clear, and when a device is free to transmit data

The way CSMA/CD works is actually pretty simple. If there's no data currently being transmitted on the network segment, a node will feel free to send data. If it turns out that two or more computers end up trying to send data at the same time, the computers detect this collision and stop sending data. Each device involved with the collision then waits a random interval of time before trying  to send data again. This random interval helps to prevent all the computers involved in the collision from colliding again the next time they try to transmit anything. When a network segment is a collision domain, it means that all devices on that segment receive all communication across the entire segment. This means we need a way to identify which node the transmission was actually meant for. This is where something known as a media access control address or MAC address comes into play.

> **MAC address**
>
> A globally unique identifier attached to an individual network interface
>
> It's a 48-bit number normally represented by six groupings of two hexadecimal numbers.

> **Hexadecimal**
>
> A way to represent numbers using 16 digits

Just like how binary is a way to represent numbers with only two digits, hexadecimal is a way to represent numbers using 16 digits. Since we don't have numerals to represent any individual digit larger than nine, hexadecimal numbers employed the letters A, B, C, D, E, and F to represent the numbers 10, 11, 12, 13, 14, and 15. 

![]({{ site.baseurl }}/images/Hexadecimal.png "Hexadecimal vs Decimal")

#### 4.2 Unicast, Multicast, and Broadcast

#### 4.3 Dissecting an Ethernet Frame




> ---
>
> The End of Week 1

