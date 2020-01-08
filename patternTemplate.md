> Use this file to gather the content required for the pattern overview. Copy this draft-patten-template.md file, replace with your own content for each of the sections below, and attach your file to the GitHub tracking issue for your pattern.

> For full details on requirements for each section, see "Write a code pattern overview" on w3 Developer: [https://w3.ibm.com/developer/documentation/write-code-pattern-overview/](https://w3.ibm.com/developer/documentation/write-code-pattern-overview/)


# Short title

> Provide a suggested short title with a maximum of 10 words. The short title must start with a task- or goal-oriented verb; for example, "Build" "Create" "Detect" "Analyze" "Implement" "Write". You can include technologies (e.g. "blockchain"), but no product names.

Build a digital asset management application using blockchain


# Long title

> Expand on the short title, focusing on open source or generic tools and programs. Include IBM product names only if that product is required in the pattern and cannot be substituted.

Use IBM Blockchain Platform and IBM Kubernetes Service to build a Node.js application that can perform management of digital assets by maintaining the assets in IBM Cloud Object Storage and accessing the assets via a web application created using VueJS.


# Author

> Provide names and IBM email addresses.

* Sandhya Nayak <snyk@us.ibm.com>


# URLs

## Github repo

> "Get the code": Provide the link to GitHub repo for the code.

"Get the code": https://github.com/IBM/Blockchain-for-maintaining-Digital-Assets


## Other URLs

> "View the demo": Provide the link to YouTube video of a recorded demo of the pattern. This is STRONGLY recommended. If you have other videos of demos or running apps, describe them here and add the URL below.

* Video URL #TODO


# Summary

> Expand on the long-title and provide context; This summary of the pattern will help the audience decide whether they should keep reading. The summary will be used to create the meta-description and excerpt, so be concise (2-3 sentences) and use keywords throughout.

> *Write 2-3 short sentences.*

Digital Asset Management Systems ensure that operations are only performed on a digital asset by individuals (or organizations) that have the right access rights and permissions for the asset.

This developer pattern shows how to set up a Digital Asset Management application with smart contracts that govern the transactions performed by registered users of the system on the digital assets maintained in the system.

# Technologies

> Provide the broad categories of technology used or demonstrated in your pattern. IBM Developer uses a standard list of essential and trending technologies identified by OMs, editors, and stakeholders. The first technology that you list will be considered the primary technology.

> To view all components see [https://developer.ibm.com/technologies/](https://developer.ibm.com/technologies/).

*   [Hyperledger Fabric v1.4](https://hyperledger-fabric.readthedocs.io/en/release-1.4/) is a platform for distributed ledger solutions, underpinned by a modular architecture that delivers high degrees of confidentiality, resiliency, flexibility, and scalability.
*   [Node.js](https://nodejs.org/en/) is an open source, cross-platform JavaScript run-time environment that executes server-side JavaScript code.
*   [Vue.js 2.6.10](https://vuejs.org) is an open-source JavaScript framework for building user interfaces and single-page applications.


# Description

> Tell the story of your code pattern: describe the problem and who might encounter it; why is your pattern the right way to overcome the challenge? Highlight interesting code features and wherever possible, describe real-world situations where a developer will benefit from using the pattern. DO NOT include detailed technical steps, instructions, and commands; they will be provided in the readme file for your code.

> *Write 3-4 paragraphs.*

A digital asset is defined as the content (an image, a music file, a document, a video file, etc.) and its metadata. The metadata could be as simple as the name of the asset, the name of the owner of the asset and the date of creation of the asset, or it could be something more complex, such as extracted speech from a video (subtitles). Digital Asset Management systems help in managing these assets by providing a means to ensure only permitted users make modifications to assets. 

The large number of users (participants) in this use case, as well as the different kinds of actions (transactions) that can be executed indicate that this is a good use case for Blockchain. Blockchain will also allow for the history of the transactions to be maintained in the ledger, thereby ensuring that there is always a chain of record for any changes that have been made to any asset.

In any Digital Asset Management system, there can be any number of users and these users can have the ability to perform various actions on the asset in the system based on the permissions they have. Examples of such actions that are being covered in this developer pattern are:

1. User registration and user login.
2. Viewing all existing assets in the system.
3. Viewing assets owned by the user that is currently logged in.
4. Uploading a new asset.
5. Deleting an existing asset.
6. Suggesting edits to an existing asset.
7. Viewing suggested edits for an asset that is owned by the user that is currently logged in.
8. Approving or denying suggeested edits for an asset that is owned by the user that is currently logged in.
9. Allowing other users the permission to update an asset owned by the user that is currently logged in.
10. Assigning another user as the owner of an asset that is owned by the user that is currently logged in.
11. Downloading assets.

# Flow

> Provide a draft architecture diagram followed by the flow steps; the architecture diagram needs to show a complete set of people, components, and technologies covered by your pattern; add numbers to the diagram that correspond with the written flow steps. The flow steps provide the  details of what happens at each stage, and the tasks performed by each component or technology; these are not steps to reproduce the code, but a description of the architecture of the code.

> Upload a draft architecture diagram to this issue. Remember to include numbers in the diagram to represent the flow steps that you provide below the diagram. A graphic designer will use your draft to create the production-ready image.

<p align="center">
  <img src="https://user-images.githubusercontent.com/8854447/71943978-65ba9600-3190-11ea-8131-31efc0db87a7.jpg">
</p>

1. The Blockchain Operator sets up the IBM Blockchain Platform service.
2. The IBM Blockchain Platform service creates a Hyperledger Fabric network on an IBM Kubernetes Service, and the Blockchain Operator installs and instantiates the smart contract on the network.
3. The Node.js application server uses the Fabric SDK to interact with the deployed network on IBM Blockchain Platform, IBM Cloud Object Storage instance and the Mailtrap Server (fake SMTP testing server) and creates APIs for a web client.
4. The Vue.js client uses the Node.js application API to interact with the network.
5. The User interacts with the Vue.js web interface to interact with the digital asset management application.


# Instructions

> Provide the high-level technical steps that a developer will complete in the pattern (the details for these steps will appear in the readme file). For example, if the developer needs to install and configure a program, step one might be "Download the code from GitHub" and step 2 might be "Configure the code on your local drive." You would provide the full technical details on how to configure the code in the readme file.

> Find the detailed steps for this pattern in the [readme file](<URL for the README.md file in your GitHub repo>). The steps will show you how to:

* Ready to get started? Check out the [README](https://github.com/IBM/Blockchain-for-maintaining-Digital-Assets/blob/master/README.md) for the step-by-step details on:

1. Clone the repo
2. Package the smart contract
3. Create the Mailtrap server
4. Create IBM Cloud services
5. Build a network
6. Deploy Blockchain for maintaining Digital Assets Smart Contract on the network
7. Connect application to the network
8. Run the application


# Components and services

> List all components and services that play a prominent role in your pattern. Components are IBM products, any open source project, or solutions that are NOT IBM Cloud Services. Services are services available in the IBM Cloud (public) Catalog.

> To view all components see [http://developer.ibm.com/components](http://developer.ibm.com/components).

> To view services, see [https://console.bluemix.net/catalog/](https://console.bluemix.net/catalog/)

* [IBM Cloud Kubernetes Service](https://cloud.ibm.com/kubernetes/catalog/cluster)

* [IBM Blockchain Platform](https://cloud.ibm.com/catalog/services/blockchain-platform)

* [IBM Blockchain Platform Extension for VS Code](https://marketplace.visualstudio.com/items?itemName=IBMBlockchain.ibm-blockchain-platform)

* [IBM Cloud Object Storage](https://cloud.ibm.com/catalog/services/cloud-object-storage)

* [Mailtrap.io](https://mailtrap.io)


# Runtimes

* Node.js


# Related IBM Developer content

* [Create a basic blockchain network using Blockchain Platform V2.0](https://developer.ibm.com/patterns/build-a-blockchain-network/): Package blockchain smart contracts, set up a Hyperledger Fabric network, and execute a Node.js app with the Hyperledger Fabric SDK to interact with the deployed network.
* [Emit events from Blockchain Platform](https://developer.ibm.com/patterns/implementing-blockchain-events-using-ibp-vscode-extension/): Learn how to emit events from a blockchain network so external applications can subscribe to them and take action.


# Related links

* [Hyperledger Fabric Docs](https://hyperledger-fabric.readthedocs.io/en/release-1.4/): Enterprise grade permissioned distributed ledger platform that offers modularity and versatility for a broad set of industry use cases.
