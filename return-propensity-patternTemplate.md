> Use this file to gather the content required for the pattern overview. Copy this draft-patten-template.md file, replace with your own content for each of the sections below, and attach your file to the GitHub tracking issue for your pattern.

> For full details on requirements for each section, see "Write a code pattern overview" on w3 Developer: [https://w3.ibm.com/developer/documentation/write-code-pattern-overview/](https://w3.ibm.com/developer/documentation/write-code-pattern-overview/)


# Short title

> Provide a suggested short title with a maximum of 10 words. The short title must start with a task- or goal-oriented verb; for example, "Build" "Create" "Detect" "Analyze" "Implement" "Write". You can include technologies (e.g. "blockchain"), but no product names.

Build a Machine Learning model for calculating the Return Propensity of an order.


# Long title

> Expand on the short title, focusing on open source or generic tools and programs. Include IBM product names only if that product is required in the pattern and cannot be substituted.

Use IBM Cloud Pak for Data and the Watson Machine Learning Add-On to build a Machine Learning model to calculate the Return Propensity of a purchased order.


# Author

> Provide names and IBM email addresses.

* Sandhya Nayak <snyk@us.ibm.com>
* Nithin Mathew <nithin10@in.ibm.com>


# URLs

## Github repo

> "Get the code": Provide the link to GitHub repo for the code.

"Get the code": https://github.com/IBM/ReturnPropensity


# Summary

> Expand on the long-title and provide context; This summary of the pattern will help the audience decide whether they should keep reading. The summary will be used to create the meta-description and excerpt, so be concise (2-3 sentences) and use keywords throughout.

> *Write 2-3 short sentences.*

In the growing era of e-commerce, products being returned amounts to a large portion of the lost revenue. Hence, the sooner we can identify the chances of an order being returned, the better equipped we are at reducing the loss of revenue, both directly and indirectly in the form of lost customers. 

This developer pattern shows how to build and deploy a machine learning model on IBM Cloud Pak for Data using Watson Studio and Watson Machine Learning. This model can then be used to predict the probability of a particular order being returned, that is, the return propensity.


# Technologies

> Provide the broad categories of technology used or demonstrated in your pattern. IBM Developer uses a standard list of essential and trending technologies identified by OMs, editors, and stakeholders. The first technology that you list will be considered the primary technology.

> To view all components see [https://developer.ibm.com/technologies/](https://developer.ibm.com/technologies/).

* [Jupyter Notebooks](https://jupyter.org): An open-source web application that allows you to create and share documents that contain live code, equations, visualizations, and explanatory text.

* [Pandas](https://pandas.pydata.org): An open source library providing high-performance, easy-to-use data structures and data analysis tools for the Python programming language.

* [Scikit-Learn](https://scikit-learn.org/stable/): An open source machine learning library providing simple and efficient tools for predictive data analysis (such as classification, regression, and clustering) for the Python programming language.


# Description

> Tell the story of your code pattern: describe the problem and who might encounter it; why is your pattern the right way to overcome the challenge? Highlight interesting code features and wherever possible, describe real-world situations where a developer will benefit from using the pattern. DO NOT include detailed technical steps, instructions, and commands; they will be provided in the readme file for your code.

> *Write 3-4 paragraphs.*

As part of the Intelligent Sterling Call Center Solution, our AI Assistant can surface real time insights about the customer's orders, based on the customer's order history and previous transactions. It also provides actionable recommendations to provide easy resolutions to common customer issues leading to an enhanced customer experience. Machine Learning models and techniques are used on the aggregated customer data from multiple data sources, to gain customer insights like Customer Life time Value, Churn, Return Propensity, and Upsell Purchase Probability. These help the Call Center executive to know the customer better, and take better business decisions like Upsell, Cross-sell, and Customer appeasement during a customer conversation. 

This code pattern demonstrates how to build and deploy a machine learning model using a dataset consisting of curated order records obtained from [IBM Sterling Order Management](https://www.ibm.com/products/order-management).

When you have completed this code pattern, you will understand how to:

* Leverage ICP4D, Watson Studio and Watson Machine Learning to build and deploy machine learning models.
* Build a model to classify returns.
* Generate predictions using the deployed model by making REST calls.


# Flow

> Provide a draft architecture diagram followed by the flow steps; the architecture diagram needs to show a complete set of people, components, and technologies covered by your pattern; add numbers to the diagram that correspond with the written flow steps. The flow steps provide the  details of what happens at each stage, and the tasks performed by each component or technology; these are not steps to reproduce the code, but a description of the architecture of the code.

> Upload a draft architecture diagram to this issue. Remember to include numbers in the diagram to represent the flow steps that you provide below the diagram. A graphic designer will use your draft to create the production-ready image.

<p align="center">
  <img src="https://user-images.githubusercontent.com/8854447/74355360-c7bb7c00-4d8a-11ea-88b4-0e9d95363c6f.png">
</p>

1. User loads the Jupyter notebook into the IBM Cloud Pak for Data platform.
2. The data set is loaded into the Jupyter Notebook, either directly from the github repo or by uploading a copy obtained from the github repo.
3. The data is preprocessed, machine learning models are built and saved to Watson Machine Learning on IBM Cloud Pak for Data.
4. The machine learning model is deployed into production on the IBM Cloud Pak for Data platform and a scoring endpoint is obtained.
5. Using the scoring endpoint, the model is used to predict the propensity of returning an order using a frontend application.


# Instructions

> Provide the high-level technical steps that a developer will complete in the pattern (the details for these steps will appear in the readme file). For example, if the developer needs to install and configure a program, step one might be "Download the code from GitHub" and step 2 might be "Configure the code on your local drive." You would provide the full technical details on how to configure the code in the readme file.

> Find the detailed steps for this pattern in the [readme file](<URL for the README.md file in your GitHub repo>). The steps will show you how to:

* Ready to get started? Check out the [README](https://github.com/IBM/ReturnPropensity/blob/master/Readme.md) for the step-by-step details on:

1. Create a new project
2. Add the dataset and custom library zip to the assets section of your project
3. Add the notebook to your project
4. Follow the steps in the notebook
    1. Load and preprocess the data
    2. Build the model
    3. Save and deploy the model
5. Test the model
6. Create a Python Flask app that uses the model


# Components and services

> List all components and services that play a prominent role in your pattern. Components are IBM products, any open source project, or solutions that are NOT IBM Cloud Services. Services are services available in the IBM Cloud (public) Catalog.

> To view all components see [http://developer.ibm.com/components](http://developer.ibm.com/components).

> To view services, see [https://console.bluemix.net/catalog/](https://console.bluemix.net/catalog/)

* [IBM Cloud Pak for Data](https://www.ibm.com/products/cloud-pak-for-data)

* [IBM Watson Machine Learning](https://www.ibm.com/cloud/machine-learning)

* [IBM Watson Studio](https://www.ibm.com/cloud/watson-studio)


# Runtimes

* Python


# Related IBM Developer content

* [Growing Order Data - Is it really an issue?](https://developer.ibm.com/components/sterling/series/growing-order-data-is-it-really-an-issue-blog-series)

* [IBM Sterling on IBM Developer](https://developer.ibm.com/components/sterling/)

* [AI Code Patterns](https://developer.ibm.com/technologies/artificial-intelligence/)

* [Data Analytics Code Patterns](https://developer.ibm.com/technologies/data-science/)


# Related links

* [AI and Data Code Pattern Playlist on YouTube](https://www.youtube.com/playlist?list=PLzUbsvIyrNfknNewObx5N7uGZ5FKH0Fde)

* [With Watson program](https://www.ibm.com/watson/with-watson/)

* [IBM Watson Studio](https://www.ibm.com/cloud/watson-studio)
