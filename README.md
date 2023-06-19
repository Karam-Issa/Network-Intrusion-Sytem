# Hybrid Network Intrusion Detection System using Machine Learning

# Overview
A network intrusion detection system (NIDS) is responsible for identifying and alerting against unauthorized or suspicious activity within a network. It constantly scans network traffic, looking for patterns or anomalies that may indicate a security breach, such as unauthorized access attempts, malware infections, or unusual network behavior. By promptly notifying security staff of potential threats, the NIDS enables further analysis and necessary precautions to mitigate security risks and safeguard the network from potential intrusions.


There are two main methods that the NIDS use for detecting suspicious activities:
1. Signature-based detection ( rule-based detection) utilises a pre-existing
database or pre-programmed list of signatures that identify particular patterns,
behaviours, or traits that are frequently associated with recognized threats or
attacks. These descriptions are called indications of compromise (IOC), and
they could include particular behaviours that frequently precede hostile
network attacks, file hashes, malicious sites, well-known byte sequences, or
even the subject lines of emails. The IDS sends an alert to inform security
staff of the potential security concern whenever network behaviour matches
one of these signatures.
2. Anomaly-based detection,uses machine learning, to identify a normalised
baseline of network behaviour and contrasts all activity with that baseline.
Every strange behaviour is seen as a threat. Every network activity is
compared to this baseline behaviour as the standard for typical system
operations. Anomaly-based IDS recognizes any odd activity that could be a
sign of a threat rather than looking for well-known indicators of compromise
(IOCs). Also, any behaviour that deviates from the norm, such as a person
signing in outside of regular business hours, an unapproved device being
added to a network, or a large number of new IP addresses trying to connect,
may raise a red signal.
The benefit of signature-based detection is that it is more accurate for well-known
assaults and processes data quickly. Nevertheless, it only identifies known threats and is
unable to find zero-day vulnerabilities. Anomaly-based detection, on the other hand, has the
ability to identify undiscovered threats and zero-day vulnerabilities. Anomaly-based detection
has the drawback of increasing the possibility of false positives because many benign
behaviours may be labelled suspicious. Due to this, it can take more time and will cost more
to look into every warning. [6]
In order to complement one another, the proposed NIDS system will be a hybrid that
includes both signature-based and anomaly-based detection methods. While anomaly-based
4
detection is good at finding unknown threats and zero-day exploits, signature-based
detection excels at recognizing known threats.


# System Purpose:
In today's increasingly technology-dependent world, the risk of security breaches and cyberattacks is on the rise. To protect networks and systems from these threats, a reliable and effective intrusion detection system is crucial. A hybrid intrusion detection system combines various detection techniques to provide a comprehensive approach to identifying and mitigating security threats. It analyzes network data, detects behavioral anomalies, and identifies well-known attack patterns to enhance cyberattack detection and prevention. Additionally, a hybrid IDS assists businesses in adhering to stringent security regulations, particularly in industries like healthcare and finance where data protection is critical. By offering a multi-layered defense against online attacks, this system helps organizations meet compliance requirements, proactively address security breaches, and safeguard valuable systems and data.

# Proposal Algorithm:
The suggested method for network intrusion detection system (NIDS) seeks to locate and
recognize probable intrusions or malicious activity within a network. The proposed algorithm
makes use of a number of methods, such as network data collection, data preprocessing,
anomaly detection, and signature-based analysis. In order to find well-known intrusion
patterns or harmful signatures, the system checks the packet content against a large
signature database.If the packet content was not found in the signature database, it will be
passed to the anomaly based detection module. Overall, the NIDS is based on the use of
statistical analysis, machine learning algorithms, or rule-based systems to identify
anomalous patterns or behaviours that could point to an intrusion.
The system generates warnings and logs pertinent data upon the discovery of questionable
activity or matches with recognized signatures. As new threats and changing network
patterns emerge, the system is built to continually update its signature database under the
supervision of the security operation centre (SOC). The system's capacity to efficiently
identify and respond to various sorts of network intrusions is improved by this dynamic
method.

# Summary of Architectural Design:
Summary of Architectural Design:
Data collection module that collects live real time network data, then will be passed to the
data preprocessing that will scale, encode and feature select the data to be ready to be
processes, after that the processed data will be passed to the signature -based detection
module that will check if the signature is found in the signature database. If the signature
was not found in the database, the processed data will be passed to the anomaly based
detection module that will apply the random forest classification model already trained and
fitted to prior data. Based on the machine learning model, it will classify each network
connection as anomaly or normal behaviour and will store them in an event log and alert the
soc for anomaly classified connections. If the soc wanted to further investigate the
suspicious event, the soc will request a system generated report in human readable format
for a final confirmation from the soc. If the soc has confirmed the impact of the event , they
can add this newly found malicious activity signature in the signature database, making the
system dynamic, and will be detected faster and more efficiently through the signature based
detection module in the NIDS.

# Usage
The final trained model, which is essential for the network intrusion detection system's functioning, can be accessed and utilized using the pickle library in Python. The trained model is stored in a file named "model(2).pkl". The pickle library enables easy serialization and deserialization of Python objects, making it convenient to save and load trained machine learning models. By loading the model using the pickle library, the intrusion detection system can make accurate predictions and effectively identify potential security threats in real-time.

# Documentation

For detailed documentation and a comprehensive overview of the projectplease refer to the "Hybrid_NIDS_Documentation.pdf" file. This document provides a complete Software Development Life Cycle (SDLC) of the project, offering in-depth insights into the system's design, implementation, and evaluation. It serves as a valuable resource for understanding the project's methodology, architecture, and research references.

# Machine Learning Notebook including code documentation

To gain a comprehensive understanding of the data set used, as well as a detailed explanation of the complete data analysis and processing pipeline, we encourage you to explore the "nidsMlModel.ipynb" file. This file provides a thorough walkthrough of the entire data processing workflow, including step-by-step explanations and corresponding code snippets. It covers data cleaning, preprocessing, feature engineering, and any necessary transformations. Additionally, the notebook includes the final testing and evaluation results, accompanied by insightful visualizations to aid in the interpretation of the findings. If you are interested in delving into the technical aspects of the machine learning model development and assessment, the "nidsMlModel.ipynb" file serves as a valuable resource.


# Contributors
Karam Issa 
Jude Hamdan
Maria Ishaq
Jood Maaroufi


