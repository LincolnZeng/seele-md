# How To Build Your Own Seele Network

## Steps to build your own seele-network

Refer to [Getting Started With Seele](Getting-Started-With-Seele.html) to start a single node

- If you need to start one or multiple nodes to form a network，modify the list in the staticNodes field found in the file nodes1.json under `go-seele\cmd\node\config`. The format for the staticNodes address is of the form “ip:port”. To add one or more addresses, use ”staticNodes”:[“ip:port”,…]，where ip address is the ip of the servers in the cluster. Do not add your own machine address as it will be invalid. The addresses must be the nodes within the cluster. Refer to pic1 and pic2.
```
"p2p": {
    "privateKey":"0xf65e40c6809643b25ce4df33153da2f3338876f181f83d2281c6ac4a987b1479",
    "staticNodes": [],
    "address": "0.0.0.0:8057",
    "networkID": 1
  }


  "p2p": {
    "privateKey":"0xf65e40c6809643b25ce4df33153da2f3338876f181f83d2281c6ac4a987b1479",
    "staticNodes": ["ip:8057","ip1:8057"],
    "address": "0.0.0.0:8057",
    "networkID": 1
  }

- For the configuration of other fields in nodes1.json, refer to **How to customize your node configurations** at [Getting Started With Seele](Getting-Started-With-Seele.html). 

- When modifications are complete, the nodes will form a cluster when started.