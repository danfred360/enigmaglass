---
layout: default
title: Components of SIEM
parent: Training Materials
nav_order: 2
---
# Components of SIEM
{: .important-title .no_toc}

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

## Components of SIEM platform
Security infrastructure and event management (SIEM) is a category of security software that helps organizations monitor, manage, and respond to security threats and events. SIEM systems typically consist of several functional components, including data aggregation, security data analytics, correlation and security event monitoring, forensic analysis, incident detection and response, real-time event response or alerting, threat intelligence, user and entity behavior analytics (UEBA), and IT compliance management. These components work together to provide organizations with a comprehensive view of their security posture, and to enable them to quickly identify and respond to potential threats.

A SIEM solution may cover all or only some of these components. Security concerns vary from company to company, and some features are only used by government systems or where they are required by law.

---

### Data Aggregation
Data Aggregation is the process of collecting data from multiple sources and organizing it into a centralized repository. This allows security analysts to have a comprehensive view of the data and make more informed decisions.

There are three major log collection methods:
- Agent-based log collection

In agent-based log collection, an agent is installed to ingest logs from a file. This doesn't require whatever is generating the logs to support logging directly to your database; instead a separate process watches for changes to the file and sends the data to your database in a secure manner.

- Agentless log collection

Agentless log collection is possible where the application that is producing the logs supports integrating with your SIEM platform directly. Basically, the agent's job is wrapped up into the existing application.

- API-based log collection

In API-based log collection, logs can be collected from network devices using an application programming interface (API) to collect the logs from the server using a process running on an entirely separate server. This separate server can then process the data it receives through the API and send it through to your database.

---

### Security Data Analytics
Security Data Analytics is the use of data analysis techniques to identify trends, patterns, and anomalies in security-related data. This can help organizations detect and respond to potential security threats in a timely manner.

---

### Correlation and Security Event Monitoring
Correlation is the process of identifying relationships between different data sets. In the context of security event management, this might involve identifying connections between different security events or between security events and other types of data, such as user activity logs, using predefined rules or machine learning.

Maintaining these predefined rules is a never-ending task as new vulnerabilities and attack vectors surface daily, so this is one of the benefits of paying for a managed SIEM solution as opposed to developing one from scratch.

---

### Forensic Analysis
Forensic Analysis is the process of collecting and analyzing data to identify the cause of a security incident and determine what happened. This is often used after an incident has occurred to help organizations understand how the incident happened and prevent similar incidents from occurring in the future.

Root cause analysis and incident reports are foundational job duties for Security Engineers. SIEM platforms make that much easier by allowing the user to "drill down" through logs of a breach or attack after the fact to determine exactly how the bad actor was able to gain access to the system.

This component of SIEM is often legally mandated.

---

### Incident Detection and Response
Incident Detection and Response involves detecting security incidents and responding to them in a timely and effective manner. This might involve deploying security tools to prevent or mitigate the incident or taking other steps to minimize the impact of the incident.

A security incident is an attempted or successful data breach in the corporate network by a bad actor. SIEM platforms detect security incidents as they happen using event correlation, user, and entity behavior  analytics (UEBA), and threat intelligence.

Once the incident has been identified, many SIEM platforms support not only triggering alerts but automated actions to neutralize the threat using predefined workflows.

This component of SIEM allows companies to lower their mean time to detect and resolve incidents.

---

### Real-time Event Response or Alerting Console
Real-time Event Response or Alerting Console is a tool that allows security personnel to monitor and respond to security events in real-time. This might involve displaying alerts and providing information about potential threats, as well as providing tools for security personnel to take action to mitigate the threat.

---

### Threat Intelligence
Threat Intelligence is information about current and emerging security threats that can help organizations protect themselves against those threats. This might include information about specific attack tactics, techniques, and procedures that are being used by threat actors, as well as information about potential vulnerabilities in an organization's systems.

There are many public and private threat intelligence feeds that can be used to obtain the contextual information that is require to identify potential security issues in the corporate system before they are exploited.

SIEM platforms can aggregate these threat intelligence feeds and provide an environment where they can be compared to the current state of the network to identify potential security vulnerabilities.

---

### User and Entity Behaviour Analytics (UEBA)
User and Entity Behaviour Analytics (UEBA) is a type of security analytics that involves analyzing user and entity behavior to identify potential security threats. This might involve analyzing data such as user activity logs and network traffic to identify unusual or suspicious behavior that could indicate a security threat.

One common form of UEBA is to train a behavior model that represents the normal operation of the corporate network. Once this baseline is set, alerts can be triggered when the network activity deviates too far from the normal behavior model. These anomalies can then be investigated further or dealt with using predefined automated rules.

UEBA differs from a correlation engine because it is not rule based. Instead, it relies on behavioral analytics.

---

### IT Compliance Management
IT Compliance Management involves ensuring that an organization's information technology systems comply with relevant laws, regulations, and standards. This might involve implementing policies and procedures to ensure that systems are secure, and that sensitive data is protected, as well as regularly auditing systems to ensure compliance.

Most companies are expected to meet certain regulations regarding data security. These regulations vary by industry and region, but normally there are fines associated with noncompliance.

Many of the components that have been covered here are required by some regulations. Companies may also need to comply with security audits by third party entities. SIEM platforms allow companies to prepare for these audits and know that they will pass ahead of time.

---

## Read more
- [SIEM Components](https://www.manageengine.com/log-management/siem/siem-components.html)
