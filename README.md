## Device Cluster

In the new WEB3 economy, end users are not only consumers of business services, but also participate in building the infrastructure that powers the services. For example, in video-centric edge computing infrastructure, community members jointly run device clusters and provide edge network transmission and computing capabilities, but these users also have access to commercial services. When they need private communication or private network transmission, and use DST’s peer-to-peer technology to share excess bandwidth, they can earn rewards and tokens. These token rewards can provide ongoing utility and benefits to holders, driving their long-term participation


![111](https://github.com/pracewol/home/assets/108162207/4d1237d7-4557-48e5-aaba-0f3a28b30ce5)

Schematic diagram of device cluster infrastructure focusing on private communication
User/Platform: The lowest layer is the cluster service node. By building cluster service nodes, it provides registration and management capabilities for application clusters, and provides underlying storage and persistence layer services for encrypted messages.

***Dst SDK***: Encapsulates the functionality of device clusters into a developer-friendly programming interface. Developers and users primarily interact with the device cluster infrastructure through this interface.

***Dst device cluster***: Provides P2P encrypted network communication cluster and is also the main user of Dst encrypted network.
Dst blockchain: Through DST's RPC interface, device clusters can interact with smart contracts deployed on DST to achieve Dao governance, incentives, online transmission proof, etc.

Integrate the communication RPC service of the service node through Dst SDK to realize private communication, address book,
Basic services such as video calls. At the same time, the SDK can realize decentralized hot updates, as well as status management and tracking of device clusters. Through the SDK, the upper structure does not need to pay too much attention to the details of the blockchain, that is, it can be controlled like the traditional application mode, and the SDK automatically completes data upload. The necessary work related to the chain and data coordination, and because of this, the SDK needs to exist as a stateful service layer.



## Install
```
<script src="dst-sdk.min.js"></script>
```

## Quick Examples
```
   const client = new DstWebSdk({ utp: false });
      const videoInfo ="ef2eaf9bc47c46ed5ebe3c1bc2b7c304ddcbf922";
      client.add(videoInfo, function (video) {
        const file = video.files.find(function (file) {
          return file.name.endsWith('.mp4')
        });
        console.log(file)

        file.renderTo("#video-container", {}, () => {
          console.log("Ready to play!");
        });
      });
````

This supports video, audio, images, PDFs, Markdown, and more, right out of the box. There are additional ways to access file content directly, including as a node-style stream, Buffer, or Blob URL.
