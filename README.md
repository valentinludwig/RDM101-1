# Introduction to Research Data Management 

These materials were prepared for the [4th ArcTrain Annual Meeting](https://www.marum.de/en/education-career/ArcTrain-2/Annual-Meeting-2017.html). The course was first held on September 12 and 13, 2017 and is structured in three blocks of lectures and exercises. The schedule is as follows:
  

09:00 - 09:15 Welcome and Overview  
09:15 - 09:45 Lecture: Research Data and Data Management Planning  
09:45 - 10:15 Exercise: Write a Data Management Plan with DMPonline  
10:15 - 10:30 Break  
10:30 - 11:00 Lecture: Working with Research Data  
11:00 - 11:30 Exercise: Versioning Data with GitHub  
11:30 - 11:45 Break  
11:45 - 12:15 Lecture: Sharing and Archiving Research Data  
12:15 - 12:45 Exercise: Archive Data with figshare and PANGAEA  
12:45 - 13:00 Closing, final questions and comments

## Welcome and Overview

Provides an [outline for the course](lectures/lecture-0/stocker17rdm101-lecture-0.pdf).

## Lecture: Research Data and Data Management Planning

The [first lecture](lectures/lecture-I/stocker17rdm101-lecture-I.pdf) introduces the notions of data, from abstract definitions to more practical ones. We looks at research data lifecycles and various data types, approaches to format and model data, as well as standardization of formats and models. We discuss the distinction between data and metadata.

## Exercise: Creating a Data Management Plan with DMPonline

[DMPonline](https://dmponline.dcc.ac.uk/) is a tool by the UK [Digital Curation Centre](http://www.dcc.ac.uk/) and the [University of California Curation Center](http://www.cdlib.org/uc3/) that supports you in creating, reviewing, and sharing data management plans that meet institutional and funder requirements.

First, create an account. If your organization is not listed, choose 'Other' and add the name of your organization, e.g. 'University of Bremen'. Once signed in, you can edit your profile. Do you have an ORCID iD? You can link it to your DMPonline profile.

The main page shows your plans, including plans that have been shared with you.

Let's create a plan. You'll need to answer a few questions so that DMPonline can setup the DMP template. Select the 'European Commission (Horizon 2020)' as funding organisation.

> Projects that participate in the [Horizon 2020 Open Research Data Pilot](https://www.openaire.eu/opendatapilot) are required to develop a Data Management Plan. Projects starting from January 2017 are by default part of the Open Data Pilot. See also the [Guidelines to the Rules on Open Access to Scientific Publications and Open Access to Research Data in Horizon 2020](http://ec.europa.eu/research/participants/data/ref/h2020/grants_manual/hi/oa_pilot/h2020-hi-oa-pilot-guide_en.pdf).

On the first page (Plan details) you find instructions on the Initial DMP, Detailed DMP and Final review DMP. The Initial DMP must be submitted (as a deliverable) within the first 6 months of the project. The Detailed DMP is meant to capture finer details and updates as the project progresses. The Final review DMP is meant for the final project review and may be suitable also for intermediate reviews. Scroll through the sections and see what kind of questions are asked.

Select the Initial DMP tab and provide some answers to the questions. As you answer questions, you will see the progress bar updating itself. DMPonline also records the time and the person that answered the question.

DMPonline supports the export of DMPs in various formats, including PDF. Try this functionality for your Initial DMP.

Explore the differences between the Initial DMP and the Detailed DMP (and Final review DMP).

DMPonline also support sharing DMPs with your collaborators. This is a useful functionality. Try to share your DMP with a fellow student. You will need her email and you can set permissions.

## Lecture: Working with Research Data

The [second lecture](lectures/lecture-II/stocker17rdm101-lecture-II.pdf) discusses aspects of working with research data, such finding and accessing data, data retrieval and reuse, relational databases and other technologies used to store and version data.

## Exercise: Versioning Data with GitHub

Git supports collaborative work on documents, typically software source code but it can be for any (text) files including articles, slides, posters---or data files.

To use Git, you need to [install Git](https://git-scm.com/downloads) on your computer and choose an online Git repository service. [GitHub](https://github.com/) is arguably the most popular. GitHub is free only for public projects, meaning that you need a paid plan if you want to manage your documents in private repositories. There are alternatives, including some that include private repositories in their free plan. [Bitbucket](https://bitbucket.org) is an example.

The course material is managed in a [GitHub repository](https://github.com/markusstocker/RDM101). The repository also contains an [example data file](https://github.com/markusstocker/RDM101/data/example.csv). The goal in this exercise is to collaboratively make changes to this file.

Let's create an account on [GitHub](https://github.com/). If you already have an account, sign in. Next, fork the course material repository to your account.

*Hint: Look for the `Fork` buttom on the top-right.*

This will "create a copy" of the lecture course material into your GitHub account.

In order to make changes, you need to clone the forked repository to your computer with the following command (substitute [YOUR_ACCOUNT_NAME] accordingly):

```
git clone https://github.com/[YOUR_ACCOUT_NAME]/RDM101.git

```

*Hint: On Windows you need to start a Git Bash.*

Now you can navigate into the RDM101/data folder and edit the `example.csv` data file. Try to change a temperature value, and save the file.

With the following command

```
git status
```

you are told about any changes in your working directory. You will see that the file `example.csv` has been modified. You can not commit this change and push it to GitHub, using the following commands

```
git commit -a -m "modified temperature value"
git push
```

In order to push, you need to provide your GitHub username and password.

Now, check the latest commit on GitHub. *Hint: Look for the latest commit id.* GitHub provides a good overview of the changes you made.

As you have corrected the data, you now want to inform the source to pull the change so that it can be integrated. For this, go to the Pull requests tab. The change can be merged; you can simple create the pull request. The source is then notified and can merge the change.

Naturally, GitHub repositories can have collaborators, which can be managed under settings. This is a way to give your collaborators rights to push and pull changes directly from your repository, thus bypassing pull requests.

## Lecture: Sharing and Archiving Research Data

The [third lecture](lectures/lecture-III/stocker17rdm101-lecture-III.pdf) explores drivers behind the Open Data movement, discusses some of the benefits and challenges of sharing data, issues such as data identification and citation, the role of data repositories.

## Exercise: Archiving data with figshare and PANGAEA

Enabling reproducibility of your research is not easy, even for in silico studies. Enabling repurposing of research data you have collected is similarly a challenge. An important subtask is to archive research data, understood broadly to include everything needed to reproduce your research (from collected observational data to software, samples, etc.). 

In order to archive research data you will need to create and publish a "release" of relevant materials. For digital data, such as datasets and software, this means creating a package that collects and documents the materials. Important here is that you make sure that, given the package, it is possible to replicate your research. Furthermore, it means publishing the package so that it can be accessed. There is a maturing infrastructure that supports you with publishing, archiving and preserving research data, often following international principles, guidelines, and best practices. 

Here we look at two online services that support publishing research data: [figshare](https://figshare.com/) and [PANGAEA](https://www.pangaea.de/). There are important differences between these two services, so that it is actually hard to compare them. PANGAEA specializes for Earth & Environmental Sciences whereas figshare does not specialize on a domain. PANGAEA specializes for research data, in particular numeric data as well as images, video and sound whereas figshare accepts, in addition, slides, software, papers, posters. Both figshare and PANGAEA support the unambiguous identification of published materials by means of DOI. PANGAEA's specialization enables the possibility of data and metadata standardization at the time of ingestion. Contrary to figshare, where data is published in its original form, PANGAEA curates and ingests submitted data into a database. As a result, data on figshare is incresibly heterogeneous in formats and data models whereas data on PANGAEA is standardized in data format and model, resulting in a data warehouse that supports powerful operation, such as data retrieval for selected parameters, time intervals and regions in space over the complete data holding.

Let's start with figshare. If you do not have an account yet, you'll need to sign up. Once signed in, explore fighare's functionality. Check out your profile and link your ORCID iD. You can complete your profile with links to social media and biographical information. Under "My data" you will see a list of data you published with figshare.

As an exercise, try to publish our `example.csv` data file (or any other file you like to try). Start by creating a new item. Upload the file and document it with metadata, e.g. title, authors, description, etc. You can save the newly created item at any time. Look at the functionalities for embargo, private link, and DOI. You can use the private link to give access to others, e.g. by sharing the link in personal communication. The displayed DOI is at first reserved. You can used it, e.g. to cite your data in an article but the DOI will only be resolvable (via doi.org) after you publish the data on figshare. Be careful here because published items can no longer be deleted! Figshare allows you to create collections, which is a useful feature to group items together, for instance because they are part of an article.

Next, let's look at PANGAEA. To submit data, you will need to register as a new user. Submitting data at PANGAEA will create a new issue in their issue tracker. The submission form is similar to the one you saw at figshare. The key difference is that you need to treat this form as you treat the form used to submit an article for review: no tests here. The reason is that the a data submission triggers a manual response with human curators that will handle the issue.

As a further exercise, check your PANGAEA profile and connect your account to your ORCID iD. Doing so will enable two things. First, you will be able to sign into PANGAEA using your ORCID credentials, as an alternative to the PANGAEA credentials. Second, as a contributor to dataset publications, you will be unambiguouly identified: your (ambiguious) name will be linked with your (unambiguous) ORCID iD. 

Finally, let's take a look at the PANGAEA data warehouse. The traditional way to search PANGAEA is by keywords and filtering by facets. The shown results are data publications (including collections). If you search for `temperature`, PANGAEA will currently find about 137K datasets. You can further filter them, e.g. in space-time. For August 2017, there are currently 8 datasets. Technically, you can select them individually, download and integrate the data. However, a query over the entire set is easier done uing the data warehouse. 

As an exercise, sign into PANGAEA, perform a keyword search, filter the results, and start the data warehouse. *Hint: The button can be found on the right hand side.* You can now select available parameters and geocodes, say date/time, latitude and longitude, etc. Select some. Note that on some parameters you can apply methods, e.g. average over the year. Start the query. The result is a file that contains the corresponding data, including the origin of values. Note that the data is compiled from multiple origins.

## Closing

Closing remarks, final questions and comments.




