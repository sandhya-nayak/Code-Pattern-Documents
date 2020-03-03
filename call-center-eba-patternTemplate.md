> Use this file to gather the content required for the pattern overview. Copy this draft-patten-template.md file, replace with your own content for each of the sections below, and attach your file to the GitHub tracking issue for your pattern.

> For full details on requirements for each section, see "Write a code pattern overview" on w3 Developer: [https://w3.ibm.com/developer/documentation/write-code-pattern-overview/](https://w3.ibm.com/developer/documentation/write-code-pattern-overview/)


# Short title

> Provide a suggested short title with a maximum of 10 words. The short title must start with a task- or goal-oriented verb; for example, "Build" "Create" "Detect" "Analyze" "Implement" "Write". You can include technologies (e.g. "blockchain"), but no product names.

Improve a customer care call center solution by incorporating an intelligent AI assistant.


# Long title

> Expand on the short title, focusing on open source or generic tools and programs. Include IBM product names only if that product is required in the pattern and cannot be substituted.

Integration of IBM Embedded Business AI (EBA) Framework into the IBM Sterling Call Center for Commerce application.


# Author

> Provide names and IBM email addresses.

* Sandhya Nayak <snyk@us.ibm.com>
* Prarthana Manikoth Jayakumar <prarmj10@in.ibm.com>


# URLs

## Github repo

> "Get the code": Provide the link to GitHub repo for the code.

"Get the code": https://github.com/IBM/Call-center-EBA


# Summary

> Expand on the long-title and provide context; This summary of the pattern will help the audience decide whether they should keep reading. The summary will be used to create the meta-description and excerpt, so be concise (2-3 sentences) and use keywords throughout.

> *Write 2-3 short sentences.*

In the growing era of e-commerce, it is imperative to enhance the interactions between a customer and a Customer Service Representative. Integration of an AI "digital twin" into a customer care call center solution will enable the CSRs to quickly and efficiently obtain information about the customer's orders and purchase histories thereby reducing query resolution time and hekp the CSRs obtain insights into the customer's e-commerce behaviors. This, in turn, lets the CSR make decisions that can help reduce issues such as customer churn and increased product order return propensity.

This developer pattern shows how to integrate the IBM Embedded Business Assistant (EBA), a smart AI, into the IBM Sterling Call Center for Commerce solution, in order to facilitate the provision of enhanced service by the Customer Service Representatives.


# Technologies

> Provide the broad categories of technology used or demonstrated in your pattern. IBM Developer uses a standard list of essential and trending technologies identified by OMs, editors, and stakeholders. The first technology that you list will be considered the primary technology.

> To view all components see [https://developer.ibm.com/technologies/](https://developer.ibm.com/technologies/).

* [Node.js](https://nodejs.org/) is an open source, cross-platform JavaScript run-time environment that executes server-side JavaScript code.


# Description

> Tell the story of your code pattern: describe the problem and who might encounter it; why is your pattern the right way to overcome the challenge? Highlight interesting code features and wherever possible, describe real-world situations where a developer will benefit from using the pattern. DO NOT include detailed technical steps, instructions, and commands; they will be provided in the readme file for your code.

> *Write 3-4 paragraphs.*

The IBM Sterling Call Center for Commerce Solution provides the Customer Service Representatives (CSRs) with access to a multitude of critical order fulfillment system features in a UI designed for a call center environment. These include order entry, item and inventory lookup, processing returns and exchanges, managing alerts and exceptions on orders, customer appeasement, reshipment and modifications of orders as well as price matches.

The IBM Sterling Call Center for Commerce experience can be enhanced by adding smart AI capabilities provided by the Embedded Business Assistant (or Embedded Business AI). The Embedded Business AI (“EBA”) framework is an open, hybrid multi-cloud deployable, omni-channel, enterprise-class, digital AI framework that can be used by developers to enable advanced domain-specific process automations for business users. Unlike other dialog management systems that use rule-based reasoning and predicate logic, with EBA you describe your business domain to the machine in a simple, consistent, complete and straightforward way. 

Integration of EBA into the IBM Sterling Call Center for Commerce application makes it easier and faster for the CSR to obtain relevant information about the customer they are interacting with and about the customer's orders and transactions. This results in quicker query resolutions and provides enriching and improved interactions between the customer and the CSR.

In this code pattern, you will understand how to integrate the Embedded Business Assistant with IBM Sterling Call Center for Commerce.


# Flow

> Provide a draft architecture diagram followed by the flow steps; the architecture diagram needs to show a complete set of people, components, and technologies covered by your pattern; add numbers to the diagram that correspond with the written flow steps. The flow steps provide the  details of what happens at each stage, and the tasks performed by each component or technology; these are not steps to reproduce the code, but a description of the architecture of the code.

> Upload a draft architecture diagram to this issue. Remember to include numbers in the diagram to represent the flow steps that you provide below the diagram. A graphic designer will use your draft to create the production-ready image.

<p align="center">
  <img alt="Architecture diagram" src="https://user-images.githubusercontent.com/8854447/75724385-4598e600-5cac-11ea-8419-fb1a8faf4568.png">
</p>

1. The user logs into the Embedded Business AI (EBA) Framework using their IBMId and generates public and private keys that can be used for programmatic access.
2. Using the generated private key and the GetAccessKey.js script available in the Github repo, the user then generates an access key and updates the key in the customer_overrides.properties file available in the Github repo.
3. Next, the user moves the updated customer_overrides.properties file as well as the extensions folder from the Github repo to the server where IBM Sterling Call Center for Commerce is deployed.
4. A new EAR is built and deployed to the IBM Websphere Application Server.
5. The IBM Websphere Application Server is restarted in order to reflect the changes as per the deployed EAR.
6. The user can now verify that the Embedded Business Assistant is integrated into the IBM Sterling Call Center for Commerce application.


# Instructions

> Provide the high-level technical steps that a developer will complete in the pattern (the details for these steps will appear in the readme file). For example, if the developer needs to install and configure a program, step one might be "Download the code from GitHub" and step 2 might be "Configure the code on your local drive." You would provide the full technical details on how to configure the code in the readme file.

> Find the detailed steps for this pattern in the [readme file](<URL for the README.md file in your GitHub repo>). The steps will show you how to:

* Ready to get started? Check out the [README](https://github.com/IBM/Call-center-EBA/blob/master/README.md) for the step-by-step details on:

1. Clone the Github repository
2. Generate access key
3. Copy properties file and extensions folder from Github repository to Sterling server
4. Build the EAR file and deploy the application to WebSphere
5. Restart WAS server
6. Start the deployed application on WAS
7. Verify the changes on IBM Sterling Call Center for Commerce


# Components and services

> List all components and services that play a prominent role in your pattern. Components are IBM products, any open source project, or solutions that are NOT IBM Cloud Services. Services are services available in the IBM Cloud (public) Catalog.

> To view all components see [http://developer.ibm.com/components](http://developer.ibm.com/components).

> To view services, see [https://console.bluemix.net/catalog/](https://console.bluemix.net/catalog/)

* [Embedded Business AI Framework](https://www.eba.ai)

* [IBM Sterling Order Management](https://www.ibm.com/products/order-management)

* [IBM Sterling Order Management Add-Ons](https://www.ibm.com/products/order-management/add-ons)

* [IBM WebSphere Application Server](https://www.ibm.com/cloud/websphere-application-server)


# Runtimes

* Node.js


# Related IBM Developer content

* [IBM Sterling enables intelligent orchestration of customer transactions across back-end record systems](https://developer.ibm.com/blogs/intelligent-customer-care-call-center/)

* [Build a machine learning model for calculating product order return propensity](https://developer.ibm.com/patterns/use-icp4d-to-build-the-machine-learning-model-for-return-propensity/)

* [Growing Order Data](https://developer.ibm.com/components/sterling/series/growing-order-data-is-it-really-an-issue-blog-series)

* [IBM Sterling on IBM Developer](https://developer.ibm.com/components/sterling/)
