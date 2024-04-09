## Subject

The subject of Detection, Response and Analysis introduces further concepts in cyber security and introduces additional key terms.

##  Assignment

1.  A Company makes daily backups of their database. The database is automatically recovered when a failure happens using the most recent available backup.

    The recovery happens on a different physical machine than the original database, and the entire process takes about 15 minutes.

    What is the RPO of the database?


2.  An automatic failover to a backup web server has been configured for a website. Because the backup has to be powered on first and has to pull the newest version of the website from GitHub, the process takes about 8 minutes. 

    What is the RTO of the website?

##  Key Terms

*IDS* -   * An IDS (Intrusion Detection System) monitors the traffic on a computer network to detect any suspicious activity.
        *  It analyzes the data flowing through the network to look for patterns and signs of abnormal behavior.
        *  The IDS compares the network activity to a set of predefined rules and patterns to identify any activity that might indicate an attack or intrusion.
        *  If the IDS detects something that matches one of these rules or patterns, it sends an alert to the system administrator.
        *  The system administrator can then investigate the alert and take action to prevent any damage or further intrusion.

*Comparison of IDS with Firewalls*
IDS and firewall both are related to network security but an IDS differs from a firewall as a firewall looks outwardly for intrusions in order to stop them from happening. 

Firewalls restrict access between networks to prevent intrusion and if an attack is from inside the network it doesn’t signal. 

An IDS describes a suspected intrusion once it has happened and then signals an alarm.

*Difference between IPS and IDS*
When IDS detects intrusion it only alerts network administration while Intrusion Prevention System(IPS) blocks the malicious packets before it reaches the destination.

*IPS*
Is a network security application that monitors network or system activities for malicious activity. Major functions of intrusion prevention systems are to identify malicious activity, collect information about this activity, report it and attempt to block or stop it. 

Intrusion prevention systems are contemplated as augmentation of Intrusion Detection Systems (IDS) because both IPS and IDS operate network traffic and system activities for malicious activity. 

IPS typically record information related to observed events, notify security administrators of important observed events and produce reports. 

Many IPS can also respond to a detected threat by attempting to prevent it from succeeding. They use various response techniques, which involve the IPS stopping the attack itself, changing the security environment or changing the attack’s content. 

*There are two main types of IPS:*

Network-Based IPS: A Network-Based IPS is installed at the network perimeter and monitors all traffic that enters and exits the network.
Host-Based IPS: A Host-Based IPS is installed on individual hosts and monitors the traffic that goes in and out of that host.

*Hack response strategies*
Preparation
Identification
Containment
Eradication
Recovery
Lessons learned

Also relevant to these steps are infomring the relevant parties (clients, regulatory bodies if relevant) and upgrading security measures to prevent similar attacks.

*Systems hardening*
Systems hardening is a collection of tools, techniques, and best practices to reduce vulnerability in technology applications, systems, infrastructure, firmware, and other areas. 

The goal of systems hardening is to reduce security risk by eliminating potential attack vectors and condensing the system’s attack surface. 

Common attack surface vulnerabilities include:

Default passwords – Attackers can leverage automated password crackers to guess the defaults. The attack surface this presents could be large if the same defaults are used across many different endpoints--from desktops to IoT--or accounts.
Hardcoded passwords and other credentials stored in plain text files can increase the attack surface in a couple important ways. If they are forgotten in deployed code or otherwise publicly exposed, the hardcoded credentials can provide a backdoor into the organization.

Unpatched software and firmware vulnerabilities are historically one of the biggest contributors to attack surfaces. While patching will mitigate a vulnerability, patches are not always available as in the case of zero day threats. Moreover, some patches may be too disruptive to implement or not economically feasible.
Lack, or deficiency, of privileged access controls. With the expansion of the cloud and all things digital transformation privileged accounts and access has exploded. The privileged account attack surface is not just humans and employees, but also increasingly involves machines and vendors. In cloud environments, privileged access and accounts may be dynamic and ephemeral, further complicating efforts to gain visibility and control over this massive risk.

Poorly configured BIOS, firewalls, ports, servers, switches, routers, or other parts of the infrastructure. With the strong growth in cloud and hybrid infrastructure, IT environments are becoming increasingly complex. This complexity is fertile ground for misconfigurations not only can cause systems to crash or misfire, but also can create dangerous security holes. Misconfigurations like open ports have resulted in some of the worst cloud breaches in recent years, such as by inadvertently exposing data buckets or providing publicly accessible backdoors to critical infrastructure

Unencrypted, or inadequately encrypted, network traffic or data at rest can make it easy for attackers to access data or eavesdrop on conversations and access and potentially gain important information (such as passwords) needed to advance an attack.

*Different types of disaster recovery options*

*Incident Response*
Incident response (sometimes called cybersecurity incident response) refers to an organization’s processes and technologies for detecting and responding to cyberthreats, security breaches or cyberattacks. A formal incident response plan enables cybersecurity teams to limit or prevent damage.

REcovery point objective (RPO) - How much data has been lost?

Recovery time objective (RTO) - How long before you're back online?

Automatic failover - the process of automatically switching your system over to another server in case the primary server(s) fail

          

##  Resources

[Geeks for Geeks IDS](https://www.geeksforgeeks.org/intrusion-detection-system-ids/)

[Geeks for Geeks IPS](https://www.geeksforgeeks.org/intrusion-prevention-system-ips/)

[National Institute of Standards and Technology](https://nvlpubs.nist.gov/nistpubs/specialpublications/nist.sp.800-61r2.pdf)

[Beyond Trust](https://www.beyondtrust.com/resources/glossary/systems-hardening#:~:text=Systems%20hardening%20is%20a%20collection,condensing%20the%20system's%20attack%20surface.)

[Geeks for Geeks System Hardening](https://www.geeksforgeeks.org/what-is-system-hardening/)

[AWS Disaster Recovery](https://docs.aws.amazon.com/whitepapers/latest/disaster-recovery-workloads-on-aws/disaster-recovery-options-in-the-cloud.html)

[Azure Disaster Backup and Recovery](https://azure.microsoft.com/en-us/solutions/backup-and-disaster-recovery)











##  Difficulties
I found it difficult to restrict my reading on this topic as I found it fascinating and wanted to learn more.  However, setting a time limit helped me to stay on track.

##  Results

1.  In the case where a compamy does daily backups, the Recovery Point Objective (how much data has been lost) will depend on the time that has passed since the most recent backup was last done and the incident taking place.  At worst, it shouldn't be more than 24hrs. So the RPO is one day.

2.  In the case where a company has an automatic failover where the latest information get's backed up from GitHub in about 8 minutes, the RTO of the company would be 8 minutes.
   
##  Learning/Reflection

##  Additional Information
I have an interest in the legislation governing cyber security and data protection in Europe, so also looked at the information below:

In Europe, there are several best practice guidelines for disaster recovery post-cyber attack. These may include:

GDPR Compliance: Ensure compliance with the General Data Protection Regulation (GDPR) requirements, which mandate data protection measures and incident response procedures.

ISO 22301: Implement the ISO 22301 standard for business continuity management systems. This framework provides guidelines for establishing, implementing, maintaining, and continually improving a business continuity management system.

ENISA Guidelines: Refer to guidelines provided by the European Union Agency for Cybersecurity (ENISA). ENISA offers resources and recommendations for enhancing cybersecurity resilience, including disaster recovery planning.

NIS Directive: Comply with the requirements of the EU Network and Information Security (NIS) Directive, which aims to enhance the cybersecurity capabilities of critical infrastructure operators and digital service providers.

Industry Standards: Adhere to industry-specific standards and regulations applicable to your sector, such as the financial services sector's regulations or healthcare industry guidelines.


