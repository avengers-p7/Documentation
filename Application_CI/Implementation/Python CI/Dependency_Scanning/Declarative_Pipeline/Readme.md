# Declarative Pipeline Python CI Depedency Scanning

  <img width="360" length="100" alt="Python" src="https://github.com/avengers-p7/Documentation/assets/156056413/ffb4fd31-eda0-4587-8774-2f694cddfec6"> 

|   Author        |  Created on   |  Version   | Last updated by  | Last edited on |
| --------------- | --------------| -----------|----------------- | -------------- |
| Vishal Kumar Kesarwani |  10-02-2024  |  Version 1 | Vishal  | 10-02-2024    |

***
## Table of Contents
+ [Introduction](#Introduction)
+ [Why Declarative Pipeline](#Why-Declarative-Pipeline)
+ [Flow Diagram](#Flow-Diagram)
+ [Pre-requisites](#Pre-requisites)
+ [Setup of Dependency Scanning](#Setup-of-Dependency-Scanning)
+ [Jenkinsfile](#Jenkinsfile)
+ [Conclusion](#Conclusion)
+ [Contact Information](#Contact-Information)
+ [Resources and References](#Resources-and-References)
  
***
## Introduction

Declarative Pipeline is a streamlined way to define Jenkins pipelines using a structured syntax within a pipeline {} block. It offers simplicity, readability, and built-in directives for defining stages, steps, and more. It integrates well with the Jenkins UI, provides pipeline visualization, and supports pipeline templates for code reuse. It's ideal for teams looking for a straightforward approach to CI/CD pipeline configuration.

***
## Why Declarative Pipeline
| Aspect          | Description                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------|
| **Organization**    | Markdown tables organize pipeline stages, descriptions, and commands into neat columns for easier readability and understanding. |
| **Readability**     | Condenses verbose Declarative Pipeline syntax, particularly beneficial for complex pipelines, enhancing readability and comprehension. |
| **Documentation**   | Integrates pipeline configuration seamlessly into project documentation using Markdown, providing a comprehensive overview of CI/CD processes. |
| **Version Control** | Markdown files are version-controlled with tools like Git, enabling tracking of pipeline changes, revision history, and collaboration. |
| **Accessibility**   | Markdown files are viewable and editable with basic text editors or online Markdown editors, facilitating review and contribution by team members, including non-technical stakeholders. |
| **Presentation**    | Markdown files can be rendered into multiple formats, including HTML, PDF, and slideshows, enabling formatted documents or presentations for sharing and presentation purposes. |

***
## Flow Diagram  
![Screenshot from 2024-02-11 00-12-01](https://github.com/avengers-p7/Documentation/assets/156056413/07ac7433-56db-46d6-94d4-ea6cc9d1bce1)


***
## Pre-requisites
| **Pre-requisites** | **Version** |
| ------------------ | ----------- |
| Jenkins | 2.426.3 | 
| Java | 17 |
| OWASP Dependency-Check | 9.0.9 |

***
## Setup of Dependency Scanning
* Follow this document for Setup [**Cilck here**](https://github.com/avengers-p7/Documentation/blob/main/Application_CI/Implementation/GolangCI/Bug%20Analysis/Declarative%20Pipeline/Readme.md#Setup)

  <img width="760" length="100" alt="Python" src="https://github.com/avengers-p7/Documentation/assets/156056413/6adc0479-6af7-475d-b142-8f647718a915"> 

* Console Output:

   <img width="760" length="100" alt="Python" src="https://github.com/avengers-p7/Documentation/assets/156056413/619d9f82-5e52-438e-9244-7bf987906dcc"> 


> [!NOTE]
> **Changes**
> *  **Pipeline name**       **-**  `Dependency_Scanning_(Python)_(Declarative)`
> *  **Jenkinsfile Path**    **-**  `Declarative Pipeline/Python/Dependency_Scanning`  

***

## HTML Report
 * Cilck [**here**](https://github.com/avengers-p7/Documentation/blob/main/Application_CI/Implementation/Python%20CI/Dependency_Scanning/Declarative_Pipeline/Report.html)

***
## Jenkinsfile
  * [**Jenkinsfie**](https://github.com/avengers-p7/Jenkinsfile/blob/main/Declarative%20Pipeline/Python/Dependency_Scanning/Jenkinsfile)
  ```shell 
pipeline {
    agent any
    
    environment {
        DEP_CHECK_VERSION = '9.0.9'
    }

    stages {
        stage('Install JDK') {
            steps {
                sh 'sudo apt update && sudo apt install -y openjdk-17-jdk'
            }
        }

        stage('Download Dependency Check') {
            steps {
                sh "wget -q https://github.com/jeremylong/DependencyCheck/releases/download/v${env.DEP_CHECK_VERSION}/dependency-check-${env.DEP_CHECK_VERSION}-release.zip"
                sh "unzip -q dependency-check-${env.DEP_CHECK_VERSION}-release.zip"
            }
        }

        stage('Clone Repository') {
            steps {
                git branch: 'main', credentialsId: 'vishal-cred', url: 'https://github.com/OT-MICROSERVICES/attendance-api.git'
            }
        }

        stage('Run Dependency Check') {
            steps {
                sh 'dependency-check/bin/dependency-check.sh --scan /var/lib/jenkins/workspace/ --out dep-check.html'
            }
        }
        stage('Clean workspace') {
            steps {
                sh "rm -rf dependency-check-${env.DEP_CHECK_VERSION}-release.zip"
                sh "rm -rf dependency-check"
            }
        }
    }
}
```
***
## Conclusion

Declarative Pipeline simplifies Jenkins pipeline configuration, offering clarity, readability, and integration with Markdown tables. It enhances collaboration, version control, and accessibility while enabling easy documentation and presentation of CI/CD processes.

***
## Contact Information
| Name | Email address |
| ---- | ------------- |
| Vishal | vishal.kesarwani.snaatak@mygurukulam.co |
***
## Resources and References
|  **Description** |   **Source** |
| ---------------- | ------------ |
| About Jenkins Pipeline (Generic Document) | [Link](https://github.com/avengers-p7/Documentation/blob/main/Application_CI/Implementation/GenericDoc/jenkinsPipeline.md  ) |
| Flow Step for create pipeline | [Link](https://github.com/avengers-p7/Documentation/blob/main/Application_CI/Design/04-%20Python%20CI%20Checks/Dependency%20Scanning/Dependency%20scanning(Python%20CI%20Checks).md) |
| POC Generic Document | [Link](https://github.com/avengers-p7/Documentation/blob/main/Application_CI/Implementation/GenericDoc/pipelinePOC.md) |
| Setup Jenkins | [Link](https://github.com/avengers-p7/Documentation/blob/main/Application_CI/Implementation/GolangCI/Bug%20Analysis/Declarative%20Pipeline/Readme.md#Setup) |
| Jenkinsfile | [Link](https://github.com/avengers-p7/Jenkinsfile/blob/main/Declarative%20Pipeline/Python/Dependency_Scanning/Jenkinsfile) |
| Scripted vs Declarative Pipelines | [Link](https://www.baeldung.com/ops/jenkins-scripted-vs-declarative-pipelines) |
| Dependency Scanning| [Link](https://github.com/avengers-p7/Documentation/blob/main/Application_CI/Design/04-%20Python%20CI%20Checks/Dependency%20Scanning/Dependency%20Scanning%20Introduction.md) |

***
