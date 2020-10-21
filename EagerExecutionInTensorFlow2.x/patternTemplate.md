> Use this file to gather the content required for the pattern overview. Copy this draft-patten-template.md file, replace with your own content for each of the sections below, and attach your file to the GitHub tracking issue for your pattern.

> For full details on requirements for each section, see "Write a code pattern overview" on w3 Developer: [https://w3.ibm.com/developer/documentation/write-code-pattern-overview/](https://w3.ibm.com/developer/documentation/write-code-pattern-overview/)


# Short title

> Provide a suggested short title with a maximum of 10 words. The short title must start with a task- or goal-oriented verb; for example, "Build" "Create" "Detect" "Analyze" "Implement" "Write". You can include technologies (e.g. "blockchain"), but no product names.

Learn about the benefits of enabling Eager Execution in TensorFlow.


# Long title

> Expand on the short title, focusing on open source or generic tools and programs. Include IBM product names only if that product is required in the pattern and cannot be substituted.

See how enabling Eager Execution in TensorFlow makes it easier to debug and understand the flow of the code without making any significant changes in the code.


# Author

> Provide names and IBM email addresses.

* Sandhya Nayak <snyk@us.ibm.com>


# URLs

## Github repo

> "Get the code": Provide the link to GitHub repo for the code.

"Get the code": https://github.com/IBM/Eager-Execution-in-TensorFlow-2.x


# Summary

> Expand on the long-title and provide context; This summary of the pattern will help the audience decide whether they should keep reading. The summary will be used to create the meta-description and excerpt, so be concise (2-3 sentences) and use keywords throughout.

> *Write 2-3 short sentences.*

TensorFlow is an end-to-end open source machine learning platform that makes it easier to build and deploy machine learning models. TensorFlow code uses a structure known as a data flow graph which is executed within a TensorFlow Session. The intermediate values of the variables in the TensorFlow graph are only evaluated within a Session. 

This means that the code cannot be debugged and the intermediate values of all variables (that is, the results of individual TensorFlow operations) are only available at the end when the entire code is run as part of a Session.

Enabling Eager Execution is the only way to obtain these intermediate results without having to run the entire code within a Session.

This developer pattern demonstrates the features of Eager Execution and the benefits of having it enabled by default in TensorFlow version 2.x.


# Technologies

> Provide the broad categories of technology used or demonstrated in your pattern. IBM Developer uses a standard list of essential and trending technologies identified by OMs, editors, and stakeholders. The first technology that you list will be considered the primary technology.

> To view all components see [https://developer.ibm.com/technologies/](https://developer.ibm.com/technologies/).

* [Jupyter Notebooks](https://jupyter.org/) is an open-source web application that allows you to create and share documents that contain live code, equations, visualizations, and explanatory text.


# Description

> Tell the story of your code pattern: describe the problem and who might encounter it; why is your pattern the right way to overcome the challenge? Highlight interesting code features and wherever possible, describe real-world situations where a developer will benefit from using the pattern. DO NOT include detailed technical steps, instructions, and commands; they will be provided in the readme file for your code.

> *Write 3-4 paragraphs.*

Due to a C/C++ backend, TensorFlow is able to run faster than pure Python code. A TensorFlow application uses a structure known as a data flow graph. In TensorFlow version 1.0, by default, every graph had to be run within a TensorFlow session. This only allowed for the entire graph to be run all at once and made it hard to debug the computation graph. The only way to get around this and be able to debug the code was to use Eager Execution.

Eager Execution is a flexible machine learning platform for research and experimentation, providing:

* An intuitive interface so the code can be structured naturally and use Python data structures. Small models and small data can be quickly iterated.
* Easier debugging by providing the ability to call operations directly to inspect code line by line and test changes.
* Natural control flow using Python control flow instead of graph control flow, which simplifies the specification of dynamic models.

With TensorFlow 2.x, Eager Execution is enabled by default. This allows TensorFlow code to be executed and evaluated line by line. 

In this code pattern, we will look at the impact of Eager Execution and the benefits of having it enabled by default in TensorFlow 2.x. We will use a Jupyter notebook to observe the behavior of TensorFlow when Eager Execution is disabled and when it is enabled.


# Flow

> Provide a draft architecture diagram followed by the flow steps; the architecture diagram needs to show a complete set of people, components, and technologies covered by your pattern; add numbers to the diagram that correspond with the written flow steps. The flow steps provide the  details of what happens at each stage, and the tasks performed by each component or technology; these are not steps to reproduce the code, but a description of the architecture of the code.

> Upload a draft architecture diagram to this issue. Remember to include numbers in the diagram to represent the flow steps that you provide below the diagram. A graphic designer will use your draft to create the production-ready image.

As part of this code pattern, you will first disable Eager Execution and run TensorFlow code to observe how Tensor operations are executed.

Next, you will restart the kernel and re-enable Eager Execution, then re-run the TensorFlow code to observe how TensorFlow operations behave differently when Eager Execution is enabled.


# Instructions

> Provide the high-level technical steps that a developer will complete in the pattern (the details for these steps will appear in the readme file). For example, if the developer needs to install and configure a program, step one might be "Download the code from GitHub" and step 2 might be "Configure the code on your local drive." You would provide the full technical details on how to configure the code in the readme file.

> Find the detailed steps for this pattern in the [readme file](<URL for the README.md file in your GitHub repo>). The steps will show you how to:

* Ready to get started? Check out the [README](https://github.com/IBM/Eager-Execution-in-TensorFlow-2.x/blob/master/README.md) for the step-by-step details on:

1. Clone the repo
2. Setup Cloud Pak for Data as a Service
3. Create a new Project and import the notebook
4. Read through the notebook
5. Run the first half of the notebook
6. Restart the kernel
7. Run the second half of the notebook


# Components and services

> List all components and services that play a prominent role in your pattern. Components are IBM products, any open source project, or solutions that are NOT IBM Cloud Services. Services are services available in the IBM Cloud (public) Catalog.

> To view all components see [http://developer.ibm.com/components](http://developer.ibm.com/components).

> To view services, see [https://console.bluemix.net/catalog/](https://console.bluemix.net/catalog/)

* [IBM Cloud Pak for Data](https://developer.ibm.com/components/cloud-pak-for-data/)

* [Watson Studio](https://developer.ibm.com/components/watson-studio/)

* [Jupyter Notebooks](https://jupyter.org/) 


# Runtimes

* Python


# Related IBM Developer content

* [An introduction to deep learning](https://developer.ibm.com/articles/an-introduction-to-deep-learning/)
