# Microsoft-Azure-Project
## HoneyPot With Microsft VM
The objective of this project was to illustrate proficiency in network security practices and the utilization of cloud resources to monitor and analyze cybersecurity threats. By configuring a honeypot within a Microsoft Azure VM, I successfully simulated an environment with deliberately open ports to attract and log unauthorized access attempts. This initiative reflects a scenario akin to what might be deployed as a defensive measure within an enterprise or educational institution's IT infrastructure.

The objective of this project was to illustrate proficiency in network security practices and the utilization of cloud resources to monitor and analyze cybersecurity threats. By configuring a honeypot within a Microsoft Azure VM, I successfully simulated an environment with deliberately open ports to attract and log unauthorized access attempts. This initiative reflects a scenario akin to what might be deployed as a defensive measure within an enterprise or educational institution's IT infrastructure inspired by a tutorial by [Josh Madakor](https://www.youtube.com/@JoshMadakor)

## Create VM in Azure while leaving the ports open to traffic (Creating an interesting target for attackers!)
![Leaving ports open in VM](https://github.com/Malikj10/Microsoft-Azure-Project/blob/main/Azure%20Project%20Screenshots/Azure%20SIEM%20project/1.%20leaving%20ports%20open%20on%20VM.png)

## Create VM in Azure this will be our honey pot!
![Create VM](https://github.com/Malikj10/Microsoft-Azure-Project/blob/main/Azure%20Project%20Screenshots/Azure%20SIEM%20project/2.%20Creating%20VM.png)

## Create Log analytics workspace in Azure for collecting, aggregating, and analyzing data from various sources.
![Create LAW](https://github.com/Malikj10/Microsoft-Azure-Project/blob/main/Azure%20Project%20Screenshots/Azure%20SIEM%20project/3.%20Creating%20Log%20analytics%20work%20space.png)

## Add VM to Log analytics workspace this provides a centralized repository for storing and querying log data, enabling deep operational insights and data-driven decisions across Azure and on-premises environments.
![Adding LAW to VM](https://github.com/Malikj10/Microsoft-Azure-Project/blob/main/Azure%20Project%20Screenshots/Azure%20SIEM%20project/4.adding%20law%20to%20VM.png)

## Add Microsoft Sentinel to Log analytics workspace. Integrating Microsoft Sentinel with an Azure Log Analytics workspace empowers it with advanced SIEM and SOAR capabilities for enhanced security analytics and threat response using the workspace's aggregated data. 
![Adding Microsoft Sentinel to Workspace](https://github.com/Malikj10/Microsoft-Azure-Project/blob/main/Azure%20Project%20Screenshots/Azure%20SIEM%20project/5.%20Adding%20sent%20to%20vm.png)

## Connect to Virtual Machine with its IP address Via RDP. 
![Connect to Virtual Machine with RDP](https://github.com/Malikj10/Microsoft-Azure-Project/blob/main/Azure%20Project%20Screenshots/Azure%20SIEM%20project/6.%20Connect%20to%20IP%20via%20RDP.png)

## Lets look at the event log in windows. In my project, I leverage the Windows Event Log, a key system feature that records system and security events, to track and analyze unauthorized access attempts and enhance my honeypot's security monitoring capabilities
![Looking at event log in VM](https://github.com/Malikj10/Microsoft-Azure-Project/blob/main/Azure%20Project%20Screenshots/Azure%20SIEM%20project/7.%20Log%20in%20View%20Events.png)

## Now we'll look at the Windows Defender firewall configuration. In my honeypot project, the default configuration of Windows Defender Firewall is selectively blocking incoming traffic, including pings, which allows me to emulate a secure system while capturing and analyzing unauthorized access attempts within the Azure VM environment.
![Looking at event Windows Defender Firewall settings in VM](https://github.com/Malikj10/Microsoft-Azure-Project/blob/main/Azure%20Project%20Screenshots/Azure%20SIEM%20project/7.%20Log%20in%20View%20Events.png)

## Now I made some changes to the firewall did you notice? For my honeypot project, I temporarily disabled the Windows Defender Firewall on the Azure VM, demonstrating the immediate change in network accessibility, as evidenced by a successful ping from my personal computer. This action serves to validate the direct effect of firewall rules on the VM's network interactions and to potentially increase its attractiveness to attackers for my security research.
![Turning off Firewall in VM](https://github.com/Malikj10/Microsoft-Azure-Project/blob/main/Azure%20Project%20Screenshots/Azure%20SIEM%20project/9.%20ICMP%20request%20getting%20through%20do%20to%20firewall%20being%20down%20now%20ready%20for%20all%20traffic.png)

## In this step, I've implemented a PowerShell script from Josh Makador's tutorial, "Custom_Security_Log_Exporter.ps1," to automatically capture and log failed Remote Desktop Protocol (RDP) connection attempts from the Windows Event Viewer. This script is instrumental in gathering detailed security data, such as geolocation, to analyze patterns of unauthorized access within my Azure VM environment.
![Running the Script in Powershell](https://github.com/Malikj10/Microsoft-Azure-Project/blob/main/Azure%20Project%20Screenshots/Azure%20SIEM%20project/11.%20The%20script%20will%20show%20the%20location%20of%20failed%20login%20attempts.png)

## I've utilized Microsoft Azure to create a custom log for consolidating failed RDP attempts and further employed Microsoft Sentinel to analyze this data with KQL queries. This approach has enabled me to transform raw security logs into structured, actionable intelligence, facilitating a deeper investigation into the attempted breaches on my honeypot system.
![Create Custom Log](https://github.com/Malikj10/Microsoft-Azure-Project/blob/main/Azure%20Project%20Screenshots/Azure%20SIEM%20project/12.%20Create%20a%20custom%20log%20to%20train%20what%20to%20look%20for.png)
![Set Up Work book For the Map](https://github.com/Malikj10/Microsoft-Azure-Project/blob/main/Azure%20Project%20Screenshots/Azure%20SIEM%20project/13.%20Set%20new%20Workbook%20for%20map%20ensure%20to%20not%20include%20sample%20data.png)

## Here I've configured a Microsoft Sentinel workbook to parse and visualize the geolocation data of failed RDP attempts using Kusto Query Language. This enables me to create a geographic heatmap of potential security threats, providing clear visual insights into the global distribution of unauthorized access attempts against my honeypot system.
![Attacks on the Workbook Map](https://github.com/Malikj10/Microsoft-Azure-Project/blob/main/Azure%20Project%20Screenshots/Azure%20SIEM%20project/14.%20you%20can%20see%20on%20the%20map%20where%20some%20failed%20logins%20have%20happened%20already.png)

## The PowerShell script I've deployed is successfully capturing and logging unauthorized brute force RDP attempts on my honeypot VM, providing real-time insights into the attack vectors used by cyber adversaries. This data is pivotal for my project, as it allows for a detailed analysis of attack patterns and strengthens the security posture of the simulated environment I've created.
![The Script is working!](https://github.com/Malikj10/Microsoft-Azure-Project/blob/main/Azure%20Project%20Screenshots/Azure%20SIEM%20project/15.%20Attacks%20coming%20in!!.png)

##  Azure Workbooks are employed to create visual representations of the data collected, exemplified by a world map that highlights the origins of failed RDP attempts. These visualizations effectively pinpoint hotspots of suspicious activities, with a concentration of attacks originating from Egypt, allowing for an at-a-glance assessment of global threat patterns against my honeypot infrastructure.
![Attacks after a few hours](https://github.com/Malikj10/Microsoft-Azure-Project/blob/main/Azure%20Project%20Screenshots/Azure%20SIEM%20project/16.%20Attacks%20after%20a%20few%20hours.png)
![Attacks after a few more hours](https://github.com/Malikj10/Microsoft-Azure-Project/blob/main/Azure%20Project%20Screenshots/Azure%20SIEM%20project/16.%20Attacks%20after%20a%20few%20hours%202.png)

## In conclusion, my project leverages the powerful capabilities of Microsoft Azure and Sentinel to collect, analyze, and visualize security threats, with a focus on unauthorized RDP access attempts. The resulting visual data provides a compelling overview of attack patterns, enabling strategic security responses. I extend my sincere thanks to Josh Makador for the valuable guidance provided through his tutorials, which have been instrumental in the success of this endeavor.





