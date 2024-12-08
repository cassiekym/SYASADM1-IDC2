![image](https://github.com/user-attachments/assets/83c68971-a58a-447b-9857-6de231812d1d)

# SYSADM1 – Monitoring Print Services in Windows Server 2019

**Requirement:** A virtual machine running Linux and Windows OS

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

![image](https://github.com/user-attachments/assets/3ad79687-838a-4346-b5ea-91f6c289618c)
![image](https://github.com/user-attachments/assets/58dedb05-9de3-45e8-9a83-45d00d6e66cf)

**SCREENSHOTS / FINDINGS:**

![image](https://github.com/user-attachments/assets/35148eb1-2cbd-42dd-818b-6a09831dd94a)
![image](https://github.com/user-attachments/assets/82f37a66-90ac-47d5-86fb-52ae3a6ebb6a)
![image](https://github.com/user-attachments/assets/687d1dcf-4cb4-40c7-ba99-016ef2ee4485)

The logs only were only listed as “Information” level. It shows the date and time the event took place and the source as “PrintService”. The task category is “Changing the default printer” on both levels with the latest event being that I changed the default printer to EPSON L210 Series (the chosen printer for deployment in this task).

![image](https://github.com/user-attachments/assets/45d3ea2f-4b30-42a9-8ac2-7de790d0f7a1)

The performance was monitored from 9:16:56 AM to 9:18:02 AM. The graph shows how much Processor (CPU) Usage are used in % Processor Time with higher values indicated to heavier CPU usage. The last value recorded in 0.036, average is 2.332, minimum is 0.000, maximum is 59.388, and the duration is 1:40 minutes.

![image](https://github.com/user-attachments/assets/3bafbb85-d9bc-4546-b2ea-8037e5f8ddc5)

**Research on Tools**

![image](https://github.com/user-attachments/assets/1b586a13-2bd1-45ce-9d08-48df0978e424)

**Comparison:**

* PrintVisor is more focused on detailed printer management, including cost tracking, user authentication, and mobile printing capabilities. It is generally more affordable for smaller setups or specific print management needs.

* Paessler PRTG provides a broader network monitoring solution that includes print monitoring as part of its feature set. While it offers robust cost analysis and alerting features, it is generally more expensive and is best suited for organizations needing extensive network monitoring beyond just printers.

**References:**

Paessler. (n.d.). *Products.* Retrieved from: https://www.paessler.com/prtg\#products

PrintVisor. (n.d). *Download printvisor.* Retrieved from: https://www.printvisor.com/download

**Installation and Configuration**

![image](https://github.com/user-attachments/assets/df333eae-bf3a-4383-b237-03dfa60fadaf)

**Reporting Findings**

![image](https://github.com/user-attachments/assets/2e4a8384-2dbd-4b89-80e3-4400471f57b4)
![image](https://github.com/user-attachments/assets/56b3674c-f52c-48c5-9b05-25423488497a)
![image](https://github.com/user-attachments/assets/a166a88c-f608-44ed-b1d1-bc792388cba9)

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
