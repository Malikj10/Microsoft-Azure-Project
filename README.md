# Microsoft-Azure-Project
# HoneyPot With Microsft VM
The objective of this project was to illustrate proficiency in network security practices and the utilization of cloud resources to monitor and analyze cybersecurity threats. By configuring a honeypot within a Microsoft Azure VM, I successfully simulated an environment with deliberately open ports to attract and log unauthorized access attempts. This initiative reflects a scenario akin to what might be deployed as a defensive measure within an enterprise or educational institution's IT infrastructure.

The objective of this project was to illustrate proficiency in network security practices and the utilization of cloud resources to monitor and analyze cybersecurity threats. By configuring a honeypot within a Microsoft Azure VM, I successfully simulated an environment with deliberately open ports to attract and log unauthorized access attempts. This initiative reflects a scenario akin to what might be deployed as a defensive measure within an enterprise or educational institution's IT infrastructure inspired by a tutorial by [Josh Madakor](https://www.youtube.com/@JoshMadakor)

## Create VM in Azure while leaving the ports open to traffic (Creating an interesting target for attackers!)
![Leaving ports open in VM](https://link)

## Create Log analytics workspace in Azure for collecting, aggregating, and analyzing data from various sources.
![Create LAW](https://link)

## Create Log analytics workspace in Azure for collecting, aggregating, and analyzing data from various sources.
![Create LAW](https://link)

## Add VM to Log analytics workspace this provides a centralized repository for storing and querying log data, enabling deep operational insights and data-driven decisions across Azure and on-premises environments.
![Adding LAW to VM](https://link)

## Add Microsoft Sentinel to Log analytics workspace. Integrating Microsoft Sentinel with an Azure Log Analytics workspace empowers it with advanced SIEM and SOAR capabilities for enhanced security analytics and threat response using the workspace's aggregated data. 
![Adding Microsoft Sentinel to Workspace](https://link)

## Connect to Virtual Machine with its IP address Via RDP. 
![Connect to Virtual Machine with RDP](https://link)

## Lets look at the event log in windows. In my project, I leverage the Windows Event Log, a key system feature that records system and security events, to track and analyze unauthorized access attempts and enhance my honeypot's security monitoring capabilities
![Looking at event log in VM](https://link)

## Now we'll look at the Windows Defender firewall configuration. In my honeypot project, the default configuration of Windows Defender Firewall is selectively blocking incoming traffic, including pings, which allows me to emulate a secure system while capturing and analyzing unauthorized access attempts within the Azure VM environment.
![Looking at event Windows Defender Firewall settings in VM](https://link)

## Now I made some changes to the firewall did you notice? For my honeypot project, I temporarily disabled the Windows Defender Firewall on the Azure VM, demonstrating the immediate change in network accessibility, as evidenced by a successful ping from my personal computer. This action serves to validate the direct effect of firewall rules on the VM's network interactions and to potentially increase its attractiveness to attackers for my security research.
![Turning off Firewall in VM](https://link)

## In this step, I've implemented a PowerShell script from Josh Makador's tutorial, "Custom_Security_Log_Exporter.ps1," to automatically capture and log failed Remote Desktop Protocol (RDP) connection attempts from the Windows Event Viewer. This script is instrumental in gathering detailed security data, such as geolocation, to analyze patterns of unauthorized access within my Azure VM environment.
![Running the Script in Powershell](https://link)

## I've utilized Microsoft Azure to create a custom log for consolidating failed RDP attempts and further employed Microsoft Sentinel to analyze this data with KQL queries. This approach has enabled me to transform raw security logs into structured, actionable intelligence, facilitating a deeper investigation into the attempted breaches on my honeypot system.
![Create Custom Log](https://link)
![Set Up Work book For the Map](https://link)

## Here I've configured a Microsoft Sentinel workbook to parse and visualize the geolocation data of failed RDP attempts using Kusto Query Language. This enables me to create a geographic heatmap of potential security threats, providing clear visual insights into the global distribution of unauthorized access attempts against my honeypot system.
![Attacks on the Workbook Map](https://link)

## The PowerShell script I've deployed is successfully capturing and logging unauthorized brute force RDP attempts on my honeypot VM, providing real-time insights into the attack vectors used by cyber adversaries. This data is pivotal for my project, as it allows for a detailed analysis of attack patterns and strengthens the security posture of the simulated environment I've created.
![The Script is working!](https://link)

##  Azure Workbooks are employed to create visual representations of the data collected, exemplified by a world map that highlights the origins of failed RDP attempts. These visualizations effectively pinpoint hotspots of suspicious activities, with a concentration of attacks originating from Egypt, allowing for an at-a-glance assessment of global threat patterns against my honeypot infrastructure.
![Attacks after a few hours](https://link)
![Attacks after a few more hours](https://link)

## In conclusion, my project leverages the powerful capabilities of Microsoft Azure and Sentinel to collect, analyze, and visualize security threats, with a focus on unauthorized RDP access attempts. The resulting visual data provides a compelling overview of attack patterns, enabling strategic security responses. I extend my sincere thanks to Josh Makador for the valuable guidance provided through his tutorials, which have been instrumental in the success of this endeavor.





