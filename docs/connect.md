# Connect to DAppNode's VPN

Once you have your DAppnode running, you will get an URL in your terminal from where you can download the VPN config file and install it on your device. Just download it and follow the instructions. For Android, Ubuntu and Windows you have to set the VPN following the instructions.

Installing (or manually setting up)this VPN file will configure your VPN connection to your DAppNode from your device. The first device VPN connection will have super admin privileges so you can access and manage the DAppnode admin UI; this user cannot be deleted.

Take into account that some VPN clients might send all traffic through the VPN, which is not very ideal if you have many people connected to your DAppNode, or only to send traffic which points to an ETH domain.

DAppNode is not intended to manage all the traffic of the devices connected to it, only the ETH domains access requests.
As a general rule, if your DAppNode is not connected through a router that supports UPnP, you will have to manually open some ports to have complete functionality. For the VPN to work you must make sure that you have opened the 4500 and 500 ports (UDP).

Here you have a sample table of the ports that should be opened in your DAppNode:

| Service       | TCP   | UDP       |
| ------------- | ----- | --------- |
| VPN           |       | 500, 4500 |
| SSH           | 22    |           |
| Ethereum Node | 30303 | 30303     |
| IPFS          | 4001  | 4002      |

If you are not able to download or install the config file, you can set it up manually following the instructions for different platforms contained in the link that the terminal gives after installation. All the parameters you need to fill in are given by your terminal when you first install it or when you connect to it vía SSH.

These are the parameters you will need to configure, still depending on your operating system follow the instructions you will find in the website you will be directed to.

<p align="center">
    <img width="300"src="https://github.com/Shelpin/DAppNode/raw/master/doc/credentialsscreen.png">
</p>

**VPN TYPE**: Select L2TP over IPSEC
**Server IP**: Select the IP given by the terminal when connecting to the DAppNode via SSH. If you are behind a router without NAT Loopback, you will also find in the terminal the internal IP you need to use to be able to connect being in the same network without NAT Loopback enabled.
**PSK**: Shared secret, you will find it in the terminal.
**VPN User**: This is the username of the super administrator and your terminal will give it to you too.
**Password**: You can also find the password in the terminal output when connecting to your DAppNode.

Now it is time…

## Enter your DAppNode

Enter https://my.admin.dnp.dappnode.eth to access DAppNode's admin interface. Bear in mind that DAppNode's functionality will be limited until the Ethereum mainnet chain is synced (should take around 2~3 hours to get a warp sync).

Now you can do things like for example:

- Navigate to a decentralized web `decentral.eth <http://decentral.eth>`\_:

- Decentralized version of `Mycrypto <http://mycrypto.dappnode.eth>`\_

- Decentralized version of `ENS Manager <http://ens.dappnode.eth>`\_

- Decentralized version of `Wallet Gnosis <http://gmultisig.dappnode.eth>`\_

- Go to IPFS by entering http://my.ipfs.dnp.dappnode.eth:5001/webui into your browser.

- You have a websocket of your parity node in ws://my.ethchain.dnp.dappnode.eth:8546 and you can use http://my.ethchain.dnp.dappnode.eth:8545 as a custom RPC to connect to metamask i.e

**NOTE ABOUT ACCESSING IPFS WEBUI:**

We have updated our IPFS package (v.0.1.4), and one of the features is to provide a more complete and user friendly web interface. The first time you access to it will ask you for your “Custom API address”, just fill the field with this address and you will be connected to your IPFS node , this is the input you have to enter in the field seen in the image below.

```
/ip4/172.33.1.5/tcp/5001
```

<p align="center">
    <img width="300"src="https://github.com/Shelpin/DAppNode/raw/master/doc/ipfsinterface.jpg">
</p>