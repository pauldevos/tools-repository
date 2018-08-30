#### <------- Note: This is in development --------> 

# devops-tools-repository
This will serve as a reservoire of [public] notes for me that outline various "infrastucture as code" thoughts and tools I've tried. I'll probably curate a number of articles that also helped shape this process.

DevOps has a crap-ton of tools. If you want your mind blown, just go here and look around [DevOpsBookMarks](http://www.devopsbookmarks.com/). A truly exhaustive resource on the number of tools out there.

The main thing is there's so many factors in how all of these tools work together. What platform are you using? AWS or Google Cloud or other or multiple cloud solutions? Is your team Ruby, Java, JavaScript or Python in terms of main tool sets? Are you looking to use stateful or procedural provisioning? e.g. can you wait 20 mins for each Docker container to spin up? How about fault tolerant solutions? All of these tools seem to address them in a slightly different way and each with a different scope of where they begin and end, e.g. Orchestration, Configuration Management, Package Management, Environment Management, Installing Software, and so on and so forth.

For the tools I'll first try to define the scope of what each tool can do. Then I'll try to show which languages each primarily uses. Lastly, learning curve to "first action" and to "proficient"...as some might be right (now) vs right (later). 

#### <------- This is in development --------> 

### Tools I'm targeting to learn or like the most so far include:
- Ansible
- Terraform
- Airflow
- Docker
- Kubernetes
- Jenkins
- Vagrant

I should note. I work a lot with Data Scientists and BI Analysts and then typically do a lot of engineering work with machine learning services (microservices). So most of my focus will be on those applications.

## Tools

A great website with a pretty extensive collection of tools organized by category type: http://www.devopsbookmarks.com/
This is an effort on my part to understand and share what tools do what within the deployment process.
  

#### DevOps - DataOps Categories

- Configuration Management
- Environment Management
- Package Management
- Infrastructure Management
- Software Provisioning
- Application Deployment

There are different types of tools that `manage` variable parts of the provisioning, configuring, envrionment, packaging, and deployment processes. This is a table to help identify which tool can do what. It does not necessarily take into account the difficulty for each category (that may come later as I understand each tool more). 

|Tool | Orchestration | Configuration| Environment| Infrastructure|Install Software | App Deployment | Package|
| ------------- | :--------:  | :--------:  |:--------:| :--------: | :--------:  | :--------: | :--------: |
| [Ansible](https://www.ansible.com/)| Yes |Yes | Yes| Very Well| No | Yes | Sort of |
| [Kubernetes](https://kubernetes.io/) | - | - |  - | - | - | - | - |
| [Docker](https://www.docker.com/what-docker) | No | Yes | No | No | Yes| No | No |
| [Terraform](https://www.terraform.io/docs/index.html)| Yes | - | - | - | - | - | - |
| CloudFormation | Yes | - | - | - | - | - | - |
| [Packer](https://www.packer.io/intro/index.html) | Yes | - | - | - | Yes | - | - |
| [Chef](https://www.chef.io/)| Yes | - | Yes | - | - | - | - |
| [Puppet](https://puppet.com/) | Yes | - | Yes | - | - | - | - |
| [SaltStack](https://saltstack.com/community/) | Yes | - | Yes | - | - | - | - |
| [Fabric](http://www.fabfile.org/) | Yes | Yes | - | - | - | - | - |
| Jenkins | - | - | - | - | - | - | - |


Configuration management tools install and manage software on servers that are provisioned. Some examples of configuration management 
tools include Chef, Puppet, Ansible, and SaltStack. 

> These two categories [orchestration and configuration management] are not mutually exclusive, as most configuration management tools can do some degree of provisioning and most 
> orchestration tools can do some degree of configuration management. But the focus on configuration management or orchestration means
> that some of the tools are going to be a better fit for certain types of tasks. - [Yevgeniy Brikman](https://blog.gruntwork.io/why-we-use-terraform-and-not-chef-puppet-ansible-saltstack-or-cloudformation-7989dad2865c)

=> Once you have an image (e.g. Docker), all you need is a server (or servers) for which to deploy the images on. Thus an orchestration tool is all you need. Terraform.
  


A more in depth look at each of the tools. These will be sublinks to other pages.

Terraform - [Use Cases](https://www.terraform.io/intro/use-cases.html)

#### Ansible
Ansible is an IT automation tool. It can configure systems, deploy software, and orchestrate more advanced IT tasks such as continuous deployments or zero downtime rolling updates.

Ansible is an open source software that automates software provisioning, configuration management, and application deployment.

In contrast with popular configuration management software — such as **Chef**, **Puppet**, and **CFEngine** — **Ansible** uses an 
*agentless* architecture. With an *agent-based* architecture, nodes must have a locally installed daemon that communicates with a 
controlling machine. With an agentless architecture, nodes are **not required to install and run background daemons** [on those endpoints] 
to connect with a controlling machine. This type of architecture reduces the overhead on the network by preventing the nodes from polling 
the controlling machine.

Ansible also uses OpenSSH and WinRM for secure network connections using network traffic encryption by providing safe tunneling 
capabilities and authentication methods. OpenSSH is also known as OpenBSD Secure Shell and is based on the Secure Shell (SSH) protocol, 
thus it is a premier connectivity tool for developers to perform remote logins through SSH protocol. Ansible automates configuration 
through pushing commands on these SSH protocols. Hence it is a push model, meaning no additional installs are not required at the end 
points.<sup>[2](#myfootnote2)</sup>

sources: 
[Wikipedia](https://en.wikipedia.org/wiki/Ansible_(software))
[Ansible and Docker: the Best Combination for an Efficient Software Product Management](https://medium.com/@cabot_solutions/ansible-and-docker-the-best-combination-for-an-efficient-software-product-management-28c86cfebe90)


1 - <a name="myfootnote1" href="https://en.wikipedia.org/wiki/Ansible_(software)">Wikipedia</a>

2- <a name="myfootnote2" href="https://medium.com/@cabot_solutions/ansible-and-docker-the-best-combination-for-an-efficient-software-product-management-28c86cfebe90">Ansible and Docker: the Best Combination for an Efficient Software Product Management</a>







[Helm](https://github.com/kubernetes/helm) - a Kubernetes Package Manager

Kubernetes
  - [Airflow on Kubernetes - Part 1](https://kubernetes.io/blog/2018/06/28/airflow-on-kubernetes-part-1-a-different-kind-of-operator/)
  - [A Friendly Introduction to Kubernetes](https://medium.freecodecamp.org/a-friendly-introduction-to-kubernetes-670c50ce4542)

Ansible
Chef
Puppet
Jenkins
Docker
  - [Docker Development Workflow](https://medium.freecodecamp.org/docker-development-workflow-a-guide-with-flask-and-postgres-db1a1843044a)


#### Python Environment Management
- Conda
- Pyenv
- venv
- virtualenv
- ?

#### Python Package Management
- Conda
- pip
- ?


Repositories
- Github
- Bitbucket
- Gitlab
 

CI/CD
- CircleCI
- TravisCI

Jupyter Hub
Docker Hub





## Workflow Schedulers, Monitors

[Airflow](https://airflow.apache.org/)
- Redis
- Postgres
- Celery

## Web Development

Python Web Frameworks
- Flask
- Django
- Tornado

Blog/CMS
- Pelican
- Wagtail


## Big Data Engineering
Spark
- PySpark
- Scala
- Performance Tuning

Dask
Pandas on Ray


Unit Testing
- pytest
- unittest
- nose

Text Editors
- Sublime
- Atom
- Nano
- Vi/Vim/Emacs

IDEs
- PyCharm

## Cloud Provisioning

AWS
- CloudFormation
- S3
- EC2
- RDS
- RedShift
- Aurora

GCP
- Cloud Storage
- Cloud SQL
- Compute Engine
- BigQuery
- Cloud Spanner




## Machine Learning

Machine Learning Algorithms
- Linear Regression
- Logistic Regression
- Decision Trees
- K-Nearest Neighbors (KNN)
- K-Means
- Support Vector Machines (SVM)
- Principal Component Analysis (PCA)
- Gradient Boost
- Neural Networks
  - CNN
  - GNN

## Deep Learning

#### Might Put these in a separate repo README (and folder) or just leave this folder as the "link farm"
Artificial Intelligence Fundamentals:
- Algebraic concepts
- Linear Algebra
- Optimization Methods
- Numerical Algorithms
- Feature Selection
- Project Structure
  - Vectorization of Data
  - Feature Engineering
  - Handling missing data and outliers, imputation
  - Train/Validation/Test
  - Metrics


## Databases (non-cloud)
- ElasticSearch
- Postgres
- Redis
- TimeScaleDB
- MongoDB
- Cassandra
- Neo4J

## Business Intelligence - Dashboarding Tools
- [Orange](https://orange.biolab.si/)
- [SuperSet](https://github.com/apache/incubator-superset)
- 





Python
- OOP (practices)
  - Types of Classes: Static, Method, Data, etc
  - Decorators
  - 4 Pillars
  - etc
- FP (practices)

- Security
  - SSH
  - VPN
  - Ports
  - PHI/PII
  - HiTRUST
  - other?

Above would link to links in format below
---- 

#### Github
Lays out understanding, tutorial, etc
Branching, Merging, Pull, Push, etc
Multiple Accounts on same computer

Cheatsheet of commands:
    - command_1
    - command_2
    - command 3
Other helpful resources:
  - subLink #1 
  - subLink #2
  - subLink #3


#### Python Environment Management
  - Link #1
  - Link #2
  - Link #3
  - Cheatsheet of commands:
    - command_1
    - command_2
    - command 3
  
  
  
Python Package Management
- tool #1
- tool #2
- tool #3

