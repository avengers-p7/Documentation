# Environment branch workflow

|   Author     |  Created on   |  Version   | Last updated by | Last edited on |
| ------------ | --------------| -----------|---------------- |--------------- |
| Vikram BISHT | 16 Jan 2024   |     v1     | Vikram Bisht    | 19 Jan 2024    |

---
# Table of Contents 
+ [Introduction](#introduction)
+ [Need of Environment Branch](#Need-of-Environment-Branch)
+ [Types of Environment Branches](#Types-of-Environment-Branches)
+ [Creating a feature branch](#Creating-a-feature-branch)
+ [Advantages](#Advantages)
+ [Disdvantages](#Disdvantages)
+ [Conclusion](#conclusion)
+ [Contact Information](#contact-information)
+ [References](#References)
***


# Introduction
In version control systems, branching is a powerful feature that allows developers to work on new features or bug fixes without affecting the main codebase. This document describes an environment branch workflow in Git, which is a popular version control system. This workflow is based on creating separate branches for different environments, such as development, staging, and production.

# Need of Environment Branch
The environment branch workflow is useful for teams that work on large projects with multiple environments. It helps to ensure that changes are properly tested and reviewed before being deployed to production. By using separate branches for each environment, teams can avoid conflicts and maintain a stable codebase.

# Types of Environment Branches

|  Types                   |        Description                                                                                                 |
| ------------             | ---------------------------------------------------------------------------------------------------------          |
| Development Branch       |  This is where all new features and bug fixes are developed and tested                                             |  
| Testing Branch           |  This environment is dedicated to comprehensive testing to identify and fix bugs before moving to the next stage   |
| Pre-Production Branch    | A dedicated environment for pre-production testing, ensuring compatibility and readiness for the live environment  |
| Staging Branch           | This environment closely mirrors the production environment and serves as a final testing ground before deployment |
| Production Branch        | The production branch contains the stable and tested code that is ready for deployment to the live environment     |

![image](https://github.com/avengers-p7/Documentation/assets/79625874/75d1cbf9-0afe-4698-949a-e29760ecb8b9)



# Creating a feature branch

* Create a new feature branch from the development branch.
* Make changes and commit them to the feature branch.
* Open a pull request to merge the feature branch into the development branch.
* Once the changes have been reviewed and tested, merge the feature branch into the staging branch.
* Test the changes in the staging environment.
* If the changes are successful, merge the staging branch into the production branch.
* Deploy the changes to the live site.

![image](https://github.com/avengers-p7/Documentation/assets/79625874/c8584f6b-f7cc-47c9-b006-0c83cd49cee9)


***
 
# Advantages

| Advantage          | Description                                                                                                     |
| ------------------ | --------------------------------------------------------------------------------------------------------------- |
| Isolation          | By using separate branches for each environment, teams can avoid conflicts and maintain a stable codebase.      |
| Testing            | Changes can be thoroughly tested in the staging environment before being deployed to production.                  |
| Review             | Pull requests allow for code reviews, which can help to catch bugs and improve code quality.                     |
| Auditing           | Environment branches provide a clear record of changes, which can be useful for auditing and debugging.           |


# Disadvantages

| Disadvantage | Description                                                                                                   |
| ------------ | ------------------------------------------------------------------------------------------------------------- |
| Complexity   | The environment branch workflow can be complex, particularly for large teams simultaneously working on multiple features. |
| Delay        | There may be a delay between making changes and deploying them to the production environment.                   |

# Conclusion 
The environment branch workflow is a useful tool for teams that work on large projects with multiple environments. By using separate branches for each environment, teams can maintain a stable codebase, thoroughly test changes, and ensure that code is reviewed before being deployed to production. However, the workflow can be complex and add overhead to the development process.


# Contact Information

|  Name                     |        	Email Address           |
| ------------              | --------------------------------|
| Vikram Bisht              |  Vikram.Bisht@opstree.com       |  

# References

|  Source                                                             |        Description                                                           |
| ------------                                                        | --------------------------------                                             |
| https://nvie.com/posts/a-successful-git-branching-model/            |  Refer to this tutorial for more information on the Feature Branch Workflow  |  
| https://github.com/avengers-p7/Documentation/blob/main/VCS/Design/FeatureBranch.md | Feature branch Doc                                            |	
