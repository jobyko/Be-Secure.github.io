
### **BeSman**
 

One of the first utilities to be created as part of the Be-Secure project is BeSman.


BeSman – is a command-line utility to provision customized environments for each open source tech stack. These environments are known as BeSman environments. We have two types of BeSman environments – **dev and sec environments**. 

The development environment is pre-bundled with all tools and dependencies that a developer would need to work on a specific open source project. Similarly, the sec environments are pre-bundled with a set of open source security tools that a security tester 

 
**Why do we need BeSman utility**

 
Individuals spend considerable effort to set up and configure the open source project in their local environment to evaluate it / commence working on it. At times individuals run into configuration issues or set up issues which result in them spending more effort to resolve them. This is a sizeable effort that is spent just to get the environment up as compared to the effort spent to build newer capability using an existing open source project. This is a misspend effort that should be managed in a better way. 
The BeSman utility provides command-line capability to provision customized environments quickly and in a consistent manner. 
 
 
**How can BeSman utility help**

 
BeSman environments are pre-bundled with tools and dependencies for a specific open project and it can be provisioned using simple bash shell commands from BeSman utility.

 
BeSman utility will also provide configurable capabilities that would permit the user to configure the tools and dependencies to be pre-bundled in the environment.

 
Individuals will have complete control over what goes into building and provisioning the environment.

 
The base BeSman environment can be customized further to address specific project needs. This gives a lot of flexibility to the developer/security  tester to optimize their work environment in a seamless manner.


#### Getting started guide

Installing BeSman using oah-shell We will be using [oah-installer](https://github.com/hyperledgerkochi/oah-installer), a component of [OpenAppHack(OAH)](https://openapphack.github.io/OAH/), to install [oah-shell](https://github.com/hyperledgerkochi/oah-shell) in the local system and using it to bring up [oah-bes-vm](https://github.com/Be-Secure/oah-bes-vm) with BeSman installed.

Pre-requisites

* Virtual Box

* Vagrant

* Ansible


Installation

1. Open your terminal

2. Execute the below command to set the correct namespace

3. export OAH_NAMESPACE=be-secure

4. Install oah-shell

5. `curl -L https://raw.githubusercontent.com/Be-secure/oah-installer/master/install.sh | bash`

6. Confirm the installation oah-shell by executing the below command which would list various oah commands

7. oah

8. Execute the below command to get the list of environments

9. oah list

**Note: Make sure oah-bes-vm is listed. If not, execute step 2 and run the below command**

    `source ${OAH_DIR}/bin/oah-init`

10. Setup oah-bes-vm for BeSman by executing the below command.

11. `oah install -v oah-bes-vm`


Testing

1. Install an environment

    `bes install -env [environment_name] -V [version]`

2. Run the below command to get the list of available enviornments

    `bes list`

3. Uninstall an environment

    `bes uninstall -env [environment_name] -V [version]`

Check out the demo video

< Video >

#### How to contribute

Be-Secure is a community first open source project that would help open source developers and security professionals to carry out security testing of different open source security technology stacks.

#### Development Activities:

* Focus on developing and provisioning new BeSman environments for different open source technology combinations

* Raise issues for existing BeSman environments to report new issues,

* Work on identified issues with BeSman environments.

* Work on feature sets to enhance security capabilities of open source security projects

#### Security Testing Activities:

* Focus on conducting security assessment of open source technologies using BeSman sec environments,

* Developing customized security testing scripts to be pre-bundled with the respective BeSman sec environment.

* Assess new open source security projects and document point of view on the respective project

* Identify new security capabilities to be developed

#### Community Activities:

* Identify new open source projects to be assessed

* Community meetups

* Creating awareness about Be-Secure project

* Maintaining Be-Secure project repositories

**Seven stage Be-Secure CE Security Assessment**

This section describes the seven stages of Be-Secure CE security assessment to enhance the security posture of open source projects / open source tech stacks.

Based on the request from the community member / user of Be-Secure project to assess an open source tech stack,

* First stage: The community will first identify the blueprint for BeSman environment using the details on the open source tech stack that has been shared.

* Second stage: If a suitable blueprint doesn’t exist, the community members will work on building a new BeSman environment. This will be the base environment to perform development activities using the shared open source tech stack.

* Third stage: The next stage will be to build the security testing environment/sandbox that can be utilized for conducting security testing for the specific open source tech stack.

* Fourth stage: Conduct security assessment based on the open source tech stack and identify the vulnerabilities in it. This vulnerability information will be published.

* Fifth stage: Identify and develop security patches for the identified vulnerabilities.

* Sixth stage: Upgrade the respective BeSman environments with the confirmed security patches to strengthen their security posture. Publish the upgraded BeSman environments for active consumption

* Seventh stage: For an existing BeSman environment, the community will focus on identifying the latest security vulnerabilities and mapping it to the respective environment. This is a continuous activity that is focused on enhancing the security posture of BeSman environments to address the latest identified vulnerabilities.

![alt text](../img/Enhance-BeSman.PNG)

### Open source Security tech stacks

We have grouped various open source technologies into 5 main categories. By doing so, it will help us to take appropriate security measures and processes to enhance the security of these open source tech stacks.

We should be able to accommodate almost all the existing open source technologies in any one of the 5 categories. The categories are defined based on the common characteristics and usage of the respective open source technologies.

![alt text](../img/techstack.PNG)


There are two environments for each tool defined under each stack:

1. **bes-<tool_dev\>-env**

    In this environment, the user will get a secure development environment. 

    eg. bes-ansibledev-env



2. **bes-<tool_sec\>-env**

    Under this environment, user will be armed with numerous security tools, to perform security testing of the techstack tools.

    eg. bes-ansiblesec-env 



At present, All tech stack and related applications are under Requirement gathering and analysis phase **(R G&A)**

Once Requirement gathering and analysis phase completed, each tech stack will be updated with another column named security status which indicates the current security vulnarabilities and fixes status of that application. 
  


## BeSman environments
&nbsp;
&nbsp;


### Security for DevOps Tools

This security stack focuses on all kinds of open source tools used in DevOps and how they can be secured both in terms of it source code and its implementation. This would enable users to implement DevSecOps using secured DevOps tools. The identified DevOps tools will be assessed for security vulnerabilities and remediated.


All are in requriment gathering and analysis Phase (R G&A)  

 >   **Ansible**

| Sl.No  | BeSman Env name                | Dependencies                             |   Entities Prebundled in BeSman Env                    |  Status 
|--------|--------------------------------|------------------------------------------|--------------------------------------------------------|-------------
| 01     | bes-ansibledev-env             | Python, Ruby, bash, ansible-galaxy       |   Git, Python, Pypi, VScode, Jenkin, Ansible-galaxy    |  R G&A  
| 02     | bes-ansiblesec-env             |                                          |   Java, Jenkin, bes-appsastsec-env, Python, Pypi       |  R G&A  


 >  **Chef**

| Sl.No  | BeSman Env name                | Dependencies                             |  Entities Prebundled in BeSman Env                     |  Status 
|--------|--------------------------------|------------------------------------------|--------------------------------------------------------|-------------
| 01     | bes-chefdev-env                | Ruby (client) and Ruby / Erlang (server) |  Git, RVM, Ruby, Erlang, VSCode, ChefSpec, Jenkin      |  R G&A  
| 02     | bes-chefsec-env                |                                          |  Git, RVM, bes-appsastsec-env, bes-appdastsec-env      |  R G&A  

Need help to view the  utility version ? [click here](./utility-catelog.md)

### Language and Framework security

This security stack focuses on all open source programming languages and its associated frameworks that are used to build various applications. These programming languages will be assessed and their vulnerabilities remediated. 

>  **Python-Django**

| Sl.No  | BeSman Env name                | Dependencies                             |  Entities Prebundled in BeSman Env                     |  Status 
|--------|--------------------------------|------------------------------------------|--------------------------------------------------------|-------------
| 01     | bes-pythonDjangodev-env        |                                          |  Git, Python, VSCode, pytest, jenkins                  |  R G&A
| 02     | bes-pythonDjangosec-env        |                                          |  Git, bes-appsastsec-env, bes-pensec-env, Pypi, Python |  R G&A


>   **Java-Spring**

| Sl.No  | BeSman Env name                | Dependencies                             |  Entities Prebundled in BeSman Env                     |  Status 
|--------|--------------------------------|------------------------------------------|--------------------------------------------------------|-------------
| 01     | bes-javaSpringdev-env          |                                          |  Git, openJDK, Apache Maven, Junit, Selenium, Jenkins  |  R G&A
| 02     | bes-javaSpringsec-env          |                                          |  Git, openJDK, bes-appsastsec-env, bes-pensec-env,     |  R G&A


Need help to view the  utility version ? [click here](./utility-catelog.md)

### Application security

This security stack focuses on all open source applications and how they can be secured.

> **Drupal**

| Sl.No  | BeSman Env name                | Dependencies                             |  Entities Prebundled in BeSman Env                           |  Status 
|--------|--------------------------------|------------------------------------------|--------------------------------------------------------------|-------------
| 01     | bes-drupaldev-env              |                                          |  TBD                                                         |  R G&A
| 02     | bes-drupalsec-env              |                                          |  TBD, bes-appsastsec-env, bes-appdastsec-env, bes-pensec-env |  R G&A


> **Odoo**

| Sl.No  | BeSman Env name                | Dependencies                             |  Entities Prebundled in BeSman Env                           |  Status 
|--------|--------------------------------|------------------------------------------|--------------------------------------------------------------|-------------
| 01     |  bes-odoodev-env               |                                          | TBD                                                          |  R G&A
| 02     |  bes-odoosec-env               |                                          | TBD, bes-appsastsec-env, bes-appdastsec-env, bes-pensec-env  |  R G&A


Need help to view the  utility version ? [click here](./utility-catelog.md)

### Distributed Application and Blockchain Security

This security stack focuses on all open source based distributed applications and blockchain frameworks. Majority of blockchain frameworks are open source in nature.

 > **Hyperledger Indy**

| Sl.No  | BeSman Env name                | Dependencies                             |  Entities Prebundled in BeSman Env                              |  Status 
|--------|--------------------------------|------------------------------------------|-----------------------------------------------------------------|-------
| 01     | bes-hyperledgerIndydev-env     |                                          | Git, Python, Pypi, VSCode, Indy-node, Indy-sdk, crypto, Jenkins | R G&A
| 02     | bes-hyperledgerIndysec-env     |                                          | TBD, bes-appsastsec-env, bes-appdastsec-env, bes-pensec-env, Git| R G&A


> **Hyperledger Fabric** 

| Sl.No  | BeSman Env name                | Dependencies                             |  Entities Prebundled in BeSman Env                             |  Status 
|--------|--------------------------------|------------------------------------------|----------------------------------------------------------------|-----------
| 01     | bes-hyperledgerFabricdev-env   |                                          |  Git, Go, NPM, Docker, NodeJS, Jnekins, Docker compose, VSCode |  R G&A
| 02     | bes-hyperledgerFabricsec-env   |                                          |  Git, Go, bes-appsastsec-env, bes-appdastsec-env, NPM, Docker  |  R G&A

Need help to view the  utility version ? [click here](./utility-catelog.md)

### open source Security Tool

This security stack focuses on all open source security tools and to secure these tools for utilization.

> **Application Security Testing (SAST )**

| Sl.No  | BeSman Env name                | Dependencies                             |  Entities Prebundled in BeSman Env                           |  Status 
|--------|--------------------------------|------------------------------------------|--------------------------------------------------------------|-------------
| 01     | bes-appsastsec-env             |                                          |  SAST-LGTM, Sonarqube, Semgrep, Gosec, OpenVAS, Vega, Grabber|  R G&A


> **Application Security Testing (DAST)**

| Sl.No  | BeSman Env name                | Dependencies                             |  Entities Prebundled in BeSman Env                           |  Status 
|--------|--------------------------------|------------------------------------------|--------------------------------------------------------------|-------------
| 01     | bes-pensec-env                 |                                          | DAST - ZAP, GoLismero, Metasploit, Burp Suite CE             | R G&A


> **Penetration Testing**

| Sl.No  | BeSman Env name                | Dependencies                             |  Entities Prebundled in BeSman Env                           |  Status 
|--------|--------------------------------|------------------------------------------|--------------------------------------------------------------|-------------
| 01     | bes-pensec-env                 |                                          | Kali Linux, Parrot Sec                                       | R G&A 

Need help to view the  utility version ? [click here](./utility-catelog.md)

 
 ### Projects we track

As part of the Be-Secure project, the community will be tracking the following projects –

* STIX Shifter

* OpenDXL Ontology

* NIST SCAP v2

* Hyperledger Fabric

* Hyperledger Indy

* Hyperledger Sawtooth

* Hyperledger BESU

* Hyperledger BURROW

* Hyperledger IROHA

* Hyperledger Aries

* Hyperledger URSA

* Hyperledger CACTUS

* Hyperledger CELLO

* Hyperledger CALIPER

* DefectDojo

* SAMM

* OWTF

* Security Shepherd Top Ten

* OWASP ZAP

* Hygieia


### Projects we contribute

As a community we will be contributing to the following projects –

* TBD

### Be-Secure Community Dashboard

* TBD