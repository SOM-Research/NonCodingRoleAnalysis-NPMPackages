# NonCodingRoleAnalysis-NPMPackages

This repository is the data companion package of the paper

> Javier Luis Cánovas Izquierdo, Jordi Cabot: On the analysis of non-coding roles in open source development. Empir. Softw. Eng. 27(1): 18 (2022)

That, as an Open Access paper, you can download from [here](https://link.springer.com/article/10.1007%2Fs10664-021-10061-x)

## Selected projects
We have collected the information for the top **100 top-starred GitHub projects with the topic _npm-package_**. 

The collection process was performed on September, 23rd 2020.

The file `repos.csv` lists the repos of the collection, ordered by number of stars.

## Structure of this repository

### ```analysis``` folder 
This folder includes the files used for the study.

#### ```repo_information.csv``` file
This file collects all the summary information from the graphs. This information has been used to answer RQ1 and first part of RQ2.

The CSV file includes the following columns:
* Repository identification: ```index```, ```repo```, ```repoType``` and ```sizeUsers```, which indicate the index, name, type (i.e., Organization or User/Individual) and number of users collaborating in the repository, respectively.  
* Role-based distribution: ```developers```,```reporters```,```mergers```,```reviewers```,```commenters``` and ```cheerleaders```, which count the number of users playing each role in the repository.
* Role-based activity: ```developer_actions```,```reporter_actions```,```merger_actions```,```reviewer_actions```, ```commenter_actions``` and ```cheerleader_actions```, which counts the number of actions per role in the repository.
* Role-based activity (percentages): ```developer_actions_perc```,```reporter_actions_perc```,```merger_actions_perc```,```reviewer_actions_perc```,```commenter_actions_perc``` and ```cheerleader_actions_perc```, which shows the ratio of actions per role in the repository.


#### ```groups_information.csv``` file

This file collects the number of role groups identified. This information has been used to answer RQ2.

The CSV file includes the following columns:
* Repository identification: ```index```, ```repo```, ```repoType``` and ```sizeUsers```, which indicates the index, name, type (i.e., Organization or User/Individual) and number of users collaborating in the repository, respectively.  
* Group information: ```group``` and ```groupSize```, which indicate the group of roles commonly found together and the number of times found in the repository.

### ```graphs``` folder 
This folder includes the collaboration graph for each repository.

For each repository, you will find:
* ```json``` file with the output of SourceCred (the tool we used to analyze each repository).
* ```pdf``` and ```png``` files are pictures of the graph (automatically generated).
* ```gml``` file is the graph in GML format.

GML and PNG files include the graphical representation of the graphs. Nodes have been colored according to this theme:

| Color  | Description |
|--------|-------------|
| Black  | Repository  |
| Blue   | Commit      | 
| Yellow | User        |
| Green  | Issue       |
| Pink   | Comment     |
| Red    | Pull Request|
| Orange | Review      |

### ```paths``` folder 
This folder contains the role migration paths for each repository. They are used to generate the Sankey diagrams. 

For each repository, you will find a CSV file with the following columns:
* Repository identification: ```index```, ```repo```, ```repoType```, which indicate the index, name, type (i.e., Organization or User/Individual) of the repository, respectively.  
* Role migration path analysis: ```path```, which indicates the role migration path found in the repository, and ```count```, which counts the number of times such a path has been found.

