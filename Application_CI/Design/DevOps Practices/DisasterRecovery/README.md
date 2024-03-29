# Disaster Recovery in Sonarqube
![image](https://github.com/avengers-p7/Documentation/assets/156056444/3fda8a89-c908-4dd2-8574-0846331fdbfc)

| Author                                                           | Created on  | Version    | Last Updated by | Last Updated on |
| ---------------------------------------------------------------- | ----------- | ---------- | --------------- | --------------- |
| **[Harshit Singh](https://github.com/Panu-S-Harshit-Ninja-07)**  | 02-02-2024  | 1.0        | Harshit Singh   | 04-02-2024      |


## Table  of Contents

1. [Introduction](#Introduction)
2. [What is Disaster Recovery?](#What-is-Disaster-Recovery)
3. [Why Disater Recovery?](#Why-Disater-Recovery)
4. [Conclusion](#Conclusion)
5. [Contact Information](#Contact-Information)
6. [References](#References)
***

## Introduction 
Disaster Recovery (DR) is crucial for organizations to swiftly respond to and recover from events impacting business operations, aiming to minimize downtime and data loss. This process involves a comprehensive analysis of IT infrastructure and the creation of a formal document for crisis management. 

This document covers what is DR, why we need it , its  types advantages and disadvantages.
***
## What is Disaster Recovery?
Disaster recovery (DR) is an organization's ability to respond to and recover from an event that negatively affects business operations. The goal of DR is to reduce downtime, data loss and operational disruptions while maintaining business continuity. To prepare for this, organizations often perform an in-depth analysis of their systems and IT infrastructure and create a formal document to follow in times of crisis. 
***
## Why Disater Recovery?
Disaster recovery is essential for organizations to ensure `business continuity, protect valuable data from loss or corruption, mitigate risks, comply with regulations, maintain customer trust and reputation, avoid financial losses, gain a competitive edge, sustain employee productivity, and stabilize supply chains`. It is a crucial strategy to swiftly recover from unexpected events or disasters and minimize the impact on operations. 

![image](https://github.com/avengers-p7/Documentation/assets/156056444/a0335bc4-61f5-4c21-9e67-61e3977195b0)
***
## How disaster recovery works
Disaster recovery relies on having a solid plan to get critical applications and infrastructure up and running after an outage—ideally within minutes.

An effective DR plan addresses three different elements for recovery: 
| Element | Description |
| ------- | --------------- |
| Preventive | Ensuring your systems are as secure and reliable as possible, using tools and techniques to prevent a disaster from occurring in the first place. This may include backing up critical data or continuously monitoring environments for configuration errors and compliance violations. 
| Detective | For rapid recovery, you’ll need to know when a response is necessary. These measures focus on detecting or discovering unwanted events as they happen in real time. 
| Corrective | These measures are aimed at planning for potential DR scenarios, ensuring backup operations to reduce impact, and putting recovery procedures into action to restore data and systems quickly when the time comes. 
***
## Types of Disaster Recovery

| Type                          | Description                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------|
| Backups                       | - Data backed up to an offsite system or external drive.                                                      |
|                               | - Not a full disaster recovery solution as it lacks IT infrastructure.                                      |
| Backup as a Service (BaaS)     | - Regular data backups provided by a third-party provider.                                                    |
| Disaster Recovery as a Service | - Cloud providers offer DRaaS, hosting data and IT infrastructure on a third-party cloud during a crisis.   |
|                               | - Provider implements and orchestrates DR plan for minimal interruption to operations.                       |
| Point-in-time Snapshots        | - Replicates data, files, or an entire database at a specific point in time.                                  |
|                               | - Used for restoring data if stored in an unaffected location, but may incur some data loss.                 |
| Virtual DR                     | - Backs up operations and data, creating a complete replica of IT infrastructure on offsite virtual machines.|
|                               | - Enables quick reload and resumption of operations after a disaster. Requires frequent data transfers.      |
| Disaster Recovery Sites        | - Temporary locations post-disaster, containing backups of data, systems, and technology infrastructure.      |
***
## Planning a disaster recovery strategy
When it comes to creating disaster recovery strategies, you should carefully consider the following key metrics: 

1. **Recovery time objective (RTO):** The maximum acceptable length of time that systems and applications can be down without causing significant damage to the business. For example, some applications can be offline for an hour, while others might need to recover in minutes.
2. **Recovery point objective (RPO):** The maximum age of data you need to recover to resume operations after a major event. RPO helps to define the frequency of backups. 

When creating your recovery strategy, it’s useful to consider your RTO and RPO values and pick a DR pattern that will enable you to meet those values and your overall goals. Typically, the smaller your values (or the faster your applications need to recover after an interruption), the higher the cost to run your application. 
***
## Advantages of DR

| Benefit                   | Description                                                                                                    |
|---------------------------|----------------------------------------------------------------------------------------------------------------|
| Stronger Business Continuity | - Minimizes business downtime, ensuring quick recovery.                                                         |
|                             | - Safeguards critical operations, preserving productivity and customer experience.                              |
| Enhanced Security          | - Strengthens security posture through data backup and other protective measures.                               |
|                             | - Cloud-based solutions offer advanced encryption, identity management, and organizational policy.             |
| Faster Recovery            | - Facilitates quicker restoration of data and workloads post-catastrophic events.                                |
|                             | - Leverages data replication and automated recovery to minimize downtime and data loss.                         |
| Reduced Recovery Costs     | - Helps avoid or minimize financial impacts of a disaster event.                                                 |
|                             | - Cloud DR processes reduce operating costs associated with maintaining a secondary location.                   |
| High Availability          | - Cloud services with High Availability (HA) features support DR strategies.                                     |
|                             | - Offers built-in redundancy and automatic failover, protecting against equipment failure and smaller events.  |
| Better Compliance          | - Supports compliance requirements by defining specific procedures and protections for data and workloads.       |
|                             | - Includes strong data backup practices, DR sites, and regular testing for preparedness.                          |
***
## Disadvantages
| Disadvantage                                       | Description                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Cost                                               | - Implementation and maintenance of DR plans can be expensive, including infrastructure and tools.  |
| Complexity                                         | - Designing and managing effective DR strategies can be complex, requiring expertise and resources.  |
| Testing Challenges                                 | - Regular testing of DR plans may disrupt normal operations and can be time-consuming.                  |
| Downtime During Implementation                      | - Implementing DR measures may cause some downtime as systems are reconfigured or data is restored.  |
| Resource Intensive                                  | - DR processes can be resource-intensive, impacting network bandwidth and system performance.         |
| Dependency on Internet Connectivity                 | - Cloud-based DR solutions depend on internet connectivity, which can be a limitation in some scenarios.|
| Data Consistency and Loss                           | - Inconsistencies or data loss may occur if DR solutions are not configured and tested properly.     |
| Limited Protection Against Human Error              | - DR plans may not fully protect against human errors in the recovery process.                         |
| Overemphasis on Technology                         | - Some organizations may focus too much on technological solutions and overlook other aspects of DR.   |
| Compliance Risks                                   | - Inadequate DR planning may lead to non-compliance with industry regulations and legal requirements. |

## Conclusion
***

## Contact Information

|     Name         | Email  |
| -----------------| ------------------------------------ |
| Harshit Singh    | harshit.singh.snaatak@mygurukulam.co |
***

## References

| Description                   | References  
| ----------------------------- | ------------------------------------------------------------------- |
| Disaster Recovery             | https://cloud.google.com/learn/what-is-disaster-recovery#:~:text=Disaster%20recovery%20(DR)%20is%20an,human%20action%20(or%20error).|
| Challenges in DR              | https://www.computerweekly.com/feature/Six-disaster-recovery-pitfalls-and-how-to-avoid-them |
