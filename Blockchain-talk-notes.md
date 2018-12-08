I am going to talk about SC in BC and how we as JS developers can make use of it. What are those things and how how the workflow would look like. I won’t have time to dive into detail of the tooling we use - technical details of BC implementation, Solidity PL or process of contract compilation because it’s already a lot to be learned. I will give you the vision of the general architecture and setup needed to create your own SC applications.

What I will be talking about:
What is SC and what are the applications of SC
What tooling is needed to development environment setup for SC development

What are ÐApps and how they can interact with smart contracts from the browser
Everyone in nowadays with interest in technology had enough time to make a bit of investigation/reading and figure out what it is so I’ll save us some time by not diving into basics. A blockchain is a distributed computing architecture where every node runs in a peer-to-peer topology, where each node executes and records the same transactions.
BC is an approach, architectural solution of some spectre of use cases if you will; directly it has nothing to do with trading some illegal assets or buying/selling some magical coins with 100s % of profit. BC do not directly require producing currency that might be traded for real money.
So, one of the projects implementing BC technology is Ethereum.

Eth started in 2013, 2015 went live. By famous Vitalik Buterin crypto and decentralisation speaker.	
Ethereum is an OS blockchain platform that allows anyone to build and use decentralized applications running on blockchain technology. Ethereum Virtual Machine (EVM) running inside every node.
A lot of newsmakers ICOs of last year also run on SC in Eth NW.

There are 2 types of accounts in Ethereum:	External Account, which has address and stores ETH balance – governed by user; and what is of peculiar interest Contract Account, which stores ETH balance and has codes – This contains the address of an instance of Smart Contract codes.			
What makes Eth so special is the ability to execute SC in it.

Besides formal definition, that was coined 20 yr ago SC - is just code that runs in Decentralised NW, and can codify real world principles.
You can see examples s such: NW democracy, voting, A Pension or Trust Fund, rating real world things or lending the money. Transparency and verification by all NW is a key point.
There are many more sophisticated SC setups.

So let’s see what it takes to write a SC. In case of Eth SCs use Solidity language to be written - Solidity is a contract-oriented, high-level language for implementing smart contracts. Solidity is statically typed, supports inheritance, libraries and complex user-defined types among other features.
So as you see the SC is a class of code that involves other contracts or reacts on called methods. Now let’s explain how this code is converted to executable form: Compilation, Bytecode, Deployment to NW.
Once the contract is deployed you can interact with it and that where the DApps come into play
Decentralized applications are apps that are built on top and connect to the blockchain. They can have various front-end interfaces, e.g., web or native. Through the interface, users interact with smart contracts used in the DApp. You can think of smart contracts as a back-end for DApps, with the blockchain being the data store.

So, let’s see what it takes to create a DApp with JS: 

Web3js - A JS bindings for BC. Similar libs exists for Python, Java, PHP etc.

Test networks and nodes (Kovan, Ropsten, etc)  or local/private networks

Private networks utilize the same technology as with live networks, but with a different configuration.

Truffle - set of tools for Built-in smart contract compilation, linking, deployment and binary management; testing; Configurable build pipeline with support for custom build processes.

Ganache CLI - a command-line version of Truffle's blockchain server.

So how to set up the dev - in older tutorial you may see ethereum-testrpc, now it’s Ganache CLI.

Actions / deployment
Take contract code: Take web app with BC bindings code
Compile and deploy contract to network
Connect to contract from JS
What you need to have it all running. Initial setup: NPM, Eth node OR Tuffle setup env, Web server

So for the demo we are going to pick one of the projects - the good ol ToDo list app. 

As you could see we had quite a basic setup and simple ToDo DApp. Later you can add more nodes and more sophisticated contracts, reuse other contacts code. There’s a bunch of good tutorials guiding you through the conf and deployment process.
As soon as you go from local private NW to test NW and the to real Eth NW - you will have many challenges:Versioning, Security audition of the contract code, etc



