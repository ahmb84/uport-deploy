# uport-deploy
A dockerized deployment of all the uport dependencies

## ethereum

https://github.com/ethereum/go-ethereum/wiki/Running-in-Docker

## ipfs

We can use the official go implementation

https://github.com/ipfs/go-ipfs


## Sensui (Fueling server)

> The fueling server, Sensui, helps new users of Ethereum overcome the initial hurdle of needing to purchase Ether to pay the fees needed to use the network. Sensui works to alleviate this problem by paying the gas fees for the user, permitting the user to create a new uPort and get up and running immediately.
The Sensui server works by utilizing the account based infrastructure of the Ethereum network. Suppose a user wants to send a transaction but they have no Ether in their sending account. The user signs the transaction as they normally would, then sends the signed transaction to the Sensui server. The server verifies that the sending account does not have enough Ether to pay for the gas, sends enough Ether to the account to pay the fees, and finally sends the user-signed transaction to the network.

There is no public reference implementation of this server. 

## Chasqui (Messaging server)

> The messaging server, Chasqui, is in charge of communication from a desktop-based decentralized application frontend to and from the mobile app. A uPort user will initially connect to a dapp by scanning the "connect with uPort" QR code. This code contains a session ID that is shared between the mobile app and the dapp frontend. When connecting with uPort the dapp frontend shows the QR code and will then poll the Chasqui server for a uPort identifier posted to the session ID. The mobile app will post the identifier and this is then immediately picked up by the dapp frontend.
Similarly when sending a transaction via the mobile app the dapp will poll the Chasqui server for a transaction hash. Once the transaction hash has been posted the dapp can immediately show that a transaction has been sent and update the UI accordingly.
Note that the Chasqui server is not used when the decentralized application is run in a mobile browser.

There is no public reference implementation of this server. 


