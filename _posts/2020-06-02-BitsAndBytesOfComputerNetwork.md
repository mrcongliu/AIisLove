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

![](../images/layers.jpg)



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

![](../images/animationOfLayers.jpg)



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

Cat5e cables have mostly replaced those older Cat5 cables because their internals reduce crosstalk.

> **Crosstalk**
>
> When an electrical pulse on one wire is accidentally detected on another wire

> **Fiber Cables**
>
> Contain individual optical fibers, which are tiny tubes made out of glass about the width of a human hair

Unlike copper, which uses electrical voltages, fiber cables use pulses of light to represent the ones and zeros of the underlying data.

Fiber cables can generally transport data quicker than copper cables can, but they're much more expensive and fragile. Fiber can also transport data over much longer distances than copper can without suffering potential data loss.