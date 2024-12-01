

|  SCHOOL OF INFORMATION AND TECHNOLOGY |  |  |
| ----- | :---- | :---: |
| NAME: MERCADO, CASSIE KYM M. | DATE PERFORMED: SEPT. 26, 2024 | /50  |
| Section: BSIT – IDC2 | DATE SUBMITTED: SEPT. 26, 2024 |  |

1. # SYSADM1 – Monitoring Print Services in Windows Server 2019

2. # Requirement: 

* A virtual machine running Linux and Windows OS

Part 1: Setting Up Print Services

1. Install and configure **print.srv** domain 

2. Connect one client to the recently created domain

3. Install Print Services Role:

4. Search the internet for any printer installer and convert it to iso

5. Install and deploy it as network printer

Part 2: Monitoring Print Services

Objective: Familiarize yourself with monitoring tools available in Windows Server 2019\.

1. Event Viewer:

   * Open Event Viewer (run eventvwr.msc).

   * Navigate to Applications and Services Logs \> Microsoft \> Windows \> PrintService.

   * Review logs for print jobs, errors, and warnings.

2. Performance Monitor:

   * Open Performance Monitor (run perfmon).

   * In the left pane, expand Data Collector Sets \> System.

   * Right-click System Performance and select Start.

   * Monitor performance metrics related to print services.

3. Using Print Management Console:

   * Open Print Management from Server Manager.

   * View active print jobs and their status.

   * Use the Printers node to check the status of all printers.

Part 3: Exploring Third-Party Monitoring Tools

1. Research at least two third-party print monitoring tools 

   * Consider factors such as features, pricing, and compatibility with Windows Server 2019\.

2. Install and Configure:

   * Choose one of the tools to install in your environment.

   * Follow the installation instructions provided by the tool's documentation.

   * Configure it to monitor your print services.

3. Test and Report Findings:

   * Generate a report or dashboard from the tool.

   * Analyze the collected data (e.g., print volume, errors, user activity).

Rubric

| Criteria | 1 (Unsatisfactory) | 2 (Needs Improvement) | 3 (Satisfactory) | 4 (Good) | 5 (Excellent) | Score |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |

| Part 1: Setting Up Print Services |  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |

| Domain Installation | No domain created | Domain created with errors | Domain created correctly | Domain configured well | Domain configured and documented thoroughly |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |

| Client Connection | Client not connected | Connection attempt failed | Client connected but with issues | Client connected correctly | Client connected and documented well |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |

| Print Services Role Installation | Role not installed | Role installed with issues | Role installed correctly | Role installed and configured | Role installed, configured, and documented thoroughly |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |

| Printer Installer Conversion | No installer found | Installer conversion attempted but failed | Installer converted but not used | Installer converted and used | Installer converted, used, and documented well |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |

| Network Printer Deployment | Printer not deployed | Deployment failed | Printer deployed but not functional | Printer deployed correctly | Printer deployed, tested, and documented well |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |

| Part 2: Monitoring Print Services |  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |

| Event Viewer Usage | Event Viewer not opened | Opened but no logs reviewed | Logs reviewed but superficial | Logs reviewed with some analysis | Logs reviewed with thorough analysis and documentation |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |

| Performance Monitor Usage | Performance Monitor not opened | Opened but no metrics monitored | Metrics monitored but not analyzed | Metrics monitored with some analysis | Metrics monitored, analyzed, and documented thoroughly |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |

| Print Management Console Usage | Console not opened | Opened but functionality not used | Active jobs viewed superficially | Active jobs viewed with some detail | Active jobs viewed and documented thoroughly |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |

| Part 3: Exploring Third-Party Tools |  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |

| Research on Tools | No tools researched | Research incomplete | Research on one tool completed | Research on two tools with some analysis | Research on two tools, detailed analysis, and comparison |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |

| Installation and Configuration | Tool not installed | Installation failed | Tool installed but not configured | Tool installed and configured with issues | Tool installed, configured, and documented thoroughly |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |

| Reporting Findings | No report generated | Report lacks detail | Report generated but lacks analysis | Report generated with some analysis | Comprehensive report with thorough analysis and documentation |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |

**SCREENSHOTS / FINDINGS:**

**Domain Installation**

**Client Connection**

**Print Services Role Installation**

	

**Printer Installer Conversion**

**Network Printer Deployment**

	

	

**Event Viewer Usage**

| Level | Date and Time | Source | Event ID | Task Category |
| ----- | ----- | ----- | ----- | ----- |
| Information | 10/3/2024 9:00:10 AM | PrintService | 823 | Changing the default printer |
| Information | 10/3/2024 9:00:10 AM | PrintService | 823 | Changing the default printer |

The logs only were only listed as “Information” level. It shows the date and time the event took place and the source as “PrintService”. The task category is “Changing the default printer” on both levels with the latest event being that I changed the default printer to EPSON L210 Series (the chosen printer for deployment in this task).

**Performance Monitor Usage**

The performance was monitored from 9:16:56 AM to 9:18:02 AM. The graph shows how much Processor (CPU) Usage are used in % Processor Time with higher values indicated to heavier CPU usage. The last value recorded in 0.036, average is 2.332, minimum is 0.000, maximum is 59.388, and the duration is 1:40 minutes.

**Print Management Console Usage**

**![][image1]**

The print management console shows the printer name, queue status, jobs, server name, and driver name.

| Printer Name | Queue Status | Jobs | Server Name | Driver Name |
| ----- | ----- | ----- | ----- | ----- |
| EPSON L210 Series | Ready | 0 | MercadoServer | Epson L210 Series |
| Microsoft XPS Document Writer | Ready | 0 | MercadoServer | Microsoft XPS Document Writer v4 |

**Research on Tools**

|  | PrintVisor | PRTG |
| :---: | ----- | ----- |
| **About** | PrintVisor is a Windows application that monitors printer usage and ink/toner levels. The program provides real-time monitoring and logging for local, virtual, and network printers. It collects data on the status of all printing devices in the organization and displays them in the application and a web dashboard. | Paessler PRTG Network Monitor is a comprehensive network monitoring solution that includes print monitoring capabilities. It helps organizations keep track of their printing infrastructure and performance, providing insights into printer usage, availability, and costs. |
| **Features** | Print Management. Allows users to manage, monitor, and control print jobs effectively Cost Tracking. Tracks printing costs per job, user, or department. User Authentication. Ensures that only authorized users can access specific users. Mobile Printing. Supports mobile printing options for users on the go. | Printer Status Monitoring. Monitors the status of network printers in real time, alerting users to any issues such as offline printers or low ink levels. Cost Analysis. Analyzes printing costs by department, user, or printer. Alerts and Notifications. Ensure prompt responses to issues like paper jams or toner shortages. Mobile Access. Access monitoring data via mobile apps, enabling on-the-go management. |
| **Pricing** | Price typically varies based on the numbers of users, printers, and specific features required. There are three options: Free, $100 per year, and $200 per year. | Price typically varies based on the numbers of users, printers, and specific features required. There are six options: Free, $2149 per year, $3899 per year, $8099 per year, $14,199 per year, and $17,899 per year. |
| **Compatibility** | PrintVisor is designed to be compatible with Windows Server 2019\. | PRTG is designed to be compatible with Windows Server 2019\. |

**Comparison:**

* PrintVisor is more focused on detailed printer management, including cost tracking, user authentication, and mobile printing capabilities. It is generally more affordable for smaller setups or specific print management needs.

* Paessler PRTG provides a broader network monitoring solution that includes print monitoring as part of its feature set. While it offers robust cost analysis and alerting features, it is generally more expensive and is best suited for organizations needing extensive network monitoring beyond just printers.

**References:**

Paessler. (n.d.). *Products.* Retrieved from: https://www.paessler.com/prtg\#products

PrintVisor. (n.d). *Download printvisor.* Retrieved from: https://www.printvisor.com/download

**Installation and Configuration**

**Reporting Findings**

Upon running the program and opening the settings, it shows that I can enable the “Show virtual printers” which prompted the Epson L210 Series and Microsoft XPS Document Writer to show up in the Printers page.

When clicking the gear icon at the right side of the selected printer. I can do the following:

* Open printer stats

* Set as default printer

* Open print queue

* Clear print queue

* Print test page

* Open device manager

* Open printer properties

  When opening the print queue, it shows the Document Name, Status, Owner, Pages, Size, and Date Submitted. When clearing the print queue, it clears the queue. When printing a test page, it prompts to save the print output. Lastly when showing the printer properties, it shows the color management, security, version information, general, sharing, ports, and advance tabs of the printer.

[image1]: <data:image/png;base64,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>