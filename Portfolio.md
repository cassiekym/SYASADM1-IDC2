![image](https://github.com/user-attachments/assets/ff7a2c72-9948-4472-8adb-bc2a7d22de65)

# **SYSADM1 PORTFOLIO**

**Table of Contents**

![image](https://github.com/user-attachments/assets/522ee3cc-344c-423a-a29a-59156e04f924)

SYSTEMS ADMINISTRATION	INSTRUCTOR: CATHERINE REYES

---

![image](https://github.com/user-attachments/assets/760afed1-99b0-4883-9a9f-badd5a50a8d5)

**SYSADM1 – Physical Infrastructure**

**Instructions:** Answer the following questions based on Week 3 Lecture notes.

1. **Identify potential issues in physical infrastructure setups and propose solutions to optimize performance or reduce costs**

![image](https://github.com/user-attachments/assets/400cb9eb-81f5-48fd-9f4d-bda58223aad0)

---
![image](https://github.com/user-attachments/assets/9d0481a6-60d3-4acb-98be-24360febf859)

**SYSADM1 – Introduction to File Systems in Windows and Linux**

**Requirement:** A virtual machine running Linux and Windows OS

Instructions:

**Part A: Windows File System**

1. **Open File Explorer:** Click the File Explorer icon on your desktop or press the Windows key \+ E.

2. **Navigate to your Documents folder:** This is usually the default location for user files.

3. **Create a new folder:** Right-click in an empty space, select "New," then "Folder." Name it "Lab1\_Windows."

![image](https://github.com/user-attachments/assets/aae2926a-5d0f-4960-a774-7640851ae3ad)

4. **Create a text file:** Right-click in the "Lab1\_Windows" folder, select "New," then "Text Document." Rename it to "info.txt."

5. **Open the text file:** Double-click the "info.txt" file to open it in Notepad.

6. **Type some text:** Write a short paragraph about yourself or the purpose of the file.

![image](https://github.com/user-attachments/assets/97c7f861-6c1b-47df-a865-202c42b6667e)

---

![image](https://github.com/user-attachments/assets/5717f0fb-50e1-44be-9d9a-07c300da662a)

**SYSADM1 – Managing Services in Windows**

**Requirement:** A virtual machine running Linux and Windows OS

**Services** are background processes that run independently of user interactions in Windows. They provide essential system functions, such as network connectivity, printing, and time synchronization. This lab will guide you through the process of managing services using the Services app.

Instructions:

1. Open the Start menu and search for "Services"

2. Familiarize yourself with the columns, including Service Name, Display Name, Status, and Startup type.

3. Right-click on a service and select "Start", "Stop", or "Restart". Fill out the table below

![image](https://github.com/user-attachments/assets/93710af4-4bf6-4f37-9e79-8730a78729dd)

---

![image](https://github.com/user-attachments/assets/3c02e679-39e0-46cf-b55c-41faf62575af)

**SYSADM1 – Monitoring Print Services in Windows Server 2019**

**Requirement:** A virtual machine running Linux and Windows OS

Part 1: Setting Up Print Services

1. Install and configure **print.srv** domain

2. Connect one client to the recently created domain

3. Install Print Services Role:

4. Search the internet for any printer installer and convert it to iso

5. Install and deploy it as network printer Part 2: Monitoring Print Services

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

   * Use the Printers node to check the status of all printers. Part 3: Exploring Third-Party Monitoring Tools

1. Research at least two third-party print monitoring tools

---

![image](https://github.com/user-attachments/assets/23e4e4a0-8d9c-47a5-ab81-ae6b2f1ccd0b)

**SYSADM1 – Setting Up Webserver**

**Requirement:** A virtual machine running Linux and Windows OS Task Instructions:

1. Install IIS by adding it as a role, select necessary features, include monitoring tools

![image](https://github.com/user-attachments/assets/cf0edb42-69b1-40fa-8f5c-19de8033a980)

---

![image](https://github.com/user-attachments/assets/d8b38ef2-7589-48a1-a59a-7993b4b6269f)

---

![image](https://github.com/user-attachments/assets/2b95699d-02cc-4cbc-9fd2-fed6332de82e)

**SYSADM1 – Kerberos Lab Activity: A step-by-step Guide**

**Objective:**

Set up a basic Kerberos authentication system to understand how Kerberos manages secure logins through ticket-based access.

**Setup Requirements:**

* Two VMs in Oracle VM, both running a Linux distribution like Ubuntu or CentOS.

  * VM1: Kerberos Server

  * VM2: Kerberos Client

  **Step 1: Initial Setup and Package Installation**

1. **Update Packages on Both VMs:**

   * Open a terminal on each VM and run:

   *bash*

   *sudo apt update && sudo apt upgrade –y*

![image](https://github.com/user-attachments/assets/36b6e8f2-1726-482f-b643-e7280d379cc3)

---

![image](https://github.com/user-attachments/assets/295c0936-9739-47a9-a063-7cdb8a9eb5ff)

**SYSADM1 – Git Basics**

Answer the following research questions about Git, GitLab desktop and GitHub.

1. What is Git, and why is it important in software development?

   Git is a distribution version control system or dVCS that was created to monitor source code modifications during software development. It is important in software development as it facilitates effective teamwork while giving developers the ability to control and manage over different versions of a project. Git allows several software developers to work on the same project at once, minimizing disputes and guaranteeing that their modifications are seamlessly incorporated. This makes Git an essential tool in software development as it supports version control, teamwork, and an organized management of code contributions.

2. How does Git track changes in a project?

   Git tracks changes and modifications made to a project by taking snapshots of the project files and keeping them in a repository. As the user edits their files, Git detects them as modified since the last commit. Once committed, Git keeps a record of the differences between the current version and the previous version by keeping a thorough and detailed history of the project's development and documenting the changes made.

3. What is the difference between a local repository and a remote repository in Git?

   A local repository contains all of the project files and version history that are kept on a developer's computer. On the other hand, a remote repository, which is hosted on a server or platform like GitHub and GitLab, is shared by multiple team members. Setting up a remote repository facilitates cooperation by enabling developers to exchange information and synchronize changes across regions. Since they are hosted on a local computer for a single user, this is not visible in a local repository.

---

![image](https://github.com/user-attachments/assets/2ee3864e-3955-49a6-be30-7ad28b550307)

**SYSADM1 – Capacity Management & Planning**

**Part 1. A Simulated Dataset for Capacity Planning Exercise**

**Scenario:** A mid-sized e-commerce website is expecting a significant surge in traffic due to an upcoming holiday sale.

![image](https://github.com/user-attachments/assets/51ef27c7-1f40-444b-b04b-1037971d6038)

Projected Traffic Increase

* **Expected Peak Traffic:** 5x the normal peak traffic  
  * **Peak Time:** 12:00 PM \- 3:00 PM on the sale day System Specifications

  * **Server Count:** 5  
  * **CPU Cores per Server:** 8  
  * **RAM per Server:** 32GB  
  * **Network Bandwidth per Server:** 1Gbps

---

![image](https://github.com/user-attachments/assets/52d91f3b-effc-4d6d-bca0-ae9ecff6d774)

* **SYSADM1 – Capacity Management & Planning Part 2\. Network Scalability Analysis**

Recall the e-commerce website scenario we discussed earlier. Given the expected surge in traffic, analyze the

provided network topology diagram. Identify potential bottlenecks and areas where scalability might be a concern. Propose specific strategies to improve the network's scalability and performance to ensure a seamless user experience during the peak traffic period. Consider factors such as increased user demand, new applications, and security threats.

![image](https://github.com/user-attachments/assets/79ad7fdd-b4f9-4758-a4ee-52c8789a3f15)

---

# **Course Reflection**

**What were your initial expectations for the course? Did the course meet, exceed, or fall short of these expectations?**

My initial expectation for the course was that SYSADM1 would build upon the previous course, SERADM1. As suggested by its description, I anticipated a greater focus on managing systems rather than just servers. The course met my expectations, as it revisited familiar topics like DNS and Print Services while introducing new ones, such as Git commands and network design. While Git commands and network design had already been covered in other courses, I was pleasantly surprised to see them included in SYSADM1 as well, providing a fresh perspective and reinforcing my understanding.

**What were the main topics or concepts covered in the course? How did these topics contribute to your understanding of the subject matter?**

The course covered a wide range of topics and concepts that deepened my understanding of system administration.

During the first grading period, we focused on identifying potential issues in physical infrastructure setups and proposing solutions. These issues included deteriorating equipment, insufficient capacity and space planning, inadequate cooling, and poor physical security. Through laboratory work, we managed file systems and created log reports on our findings. We also learned to manage Windows services, including starting, stopping, restarting, and pausing them.

In the midterms, we explored print service monitoring, including installing and deploying network printers and using third-party software to track printer statistics. We also set up our own web servers by installing IIS. A collaborative group activity required us to navigate and configure specific servers (Web, File, Directory, or Database) based on clues from strips of paper, which was both engaging and practical.

During the finals, we conducted a Kerberos lab activity, where we used various Linux commands to install and configure Kerberos. We also tackled capacity planning tasks, managing capacity, identifying bottlenecks, and proposing solutions. One of the highlights was redesigning a network to make it scalable, which I particularly enjoyed as it challenged my partner and me to think creatively about restructuring the network. Additionally, we researched various Git commands to prepare for our portfolio submission.

These topics significantly contributed to my understanding of system administration, as they covered essential areas like file maintenance, web servers, directories, databases, and repositories. Each activity reinforced practical knowledge and skills, bridging theoretical concepts with real-world applications.

**Reflecting on your learning process, what were the most effective strategies or techniques that helped you grasp and retain the course material?**

The most effective strategies for grasping and retaining the course material were teamwork and collaboration. During laboratory sessions, we often encountered challenging problems that required a deeper understanding to resolve. Collaborating with classmates allowed us to pool our knowledge and tackle these issues more effectively. Another valuable technique was troubleshooting. By systematically identifying and addressing the root causes of problems, I gained a better understanding of the material and improved my problem-solving skills.

**Were there any particular assignments, projects, or activities that significantly enhanced your learning experience? Why were they effective?**

One activity that significantly enhanced my learning experience took place during lecture hours, where we were given strips of paper and tasked with finding and working on a specific server (File, Directory, Web, or Database). This activity was particularly effective because it required critical thinking and fostered collaboration with classmates I hadn’t worked with before. It not only deepened my understanding of server roles but also built a sense of camaraderie and made the learning process more enjoyable and engaging.

**Did you encounter any challenges or difficulties during the course? How did you overcome these obstacles, and what did you learn from them?**

One significant challenge I encountered during the course was during the laboratory activity of installing a printer. Although there are numerous printer driver installers available online, finding one that was compatible with the Oracle VirtualBox machine proved to be difficult. To overcome this obstacle, I conducted further research on different printers and brands and relied on a process of trial and error to identify a solution.

From this experience, I learned the importance of perseverance and the value of thorough research. It reinforced the idea that any task can be accomplished with hard work, patience, and determination. This lesson has not only enhanced my technical problem-solving skills but also strengthened my resilience in the face of challenges.

**Did the course encourage critical thinking and analysis? How did it promote higher-order thinking skills, such as problem-solving or decision-making?**

Yes, the course actively encouraged critical thinking and analysis. It promoted higher-order thinking skills, such as problem-solving and decision-making, by incorporating situational-based requirements into many of our tasks. These scenarios challenged us to evaluate problems, analyze potential solutions, and make informed decisions based on the context. This approach not only strengthened our ability to think critically but also prepared us to apply these skills in real-world situations.

**Reflecting on your personal growth, what new knowledge, skills, or perspectives did you gain from this course?**

Reflecting on my personal growth, I gained valuable knowledge in areas such as file systems, web servers, network design, capacity management, physical infrastructure, and Git commands. In terms of skills, I improved my ability to collaborate effectively with my classmates, which enhanced both teamwork and problem-solving abilities.

From a broader perspective, I developed a deeper appreciation for how these concepts and skills interconnect, reinforcing the importance of system administration in ensuring efficient and reliable operations. This experience has motivated me to continue expanding my understanding and applying these learnings in future challenges.

**How do you plan to apply what you have learned in this course to your future studies, career, or personal life?**

I plan to apply the knowledge and skills gained from this course to my future studies, career, and personal life in several ways. The course provided me with a solid foundation in understanding and managing various systems, which are directly relevant to my chosen career path. Additionally, the activities that required personal growth, critical thinking, and decision-making have equipped me with valuable skills that can be applied beyond technical tasks. These experiences will help me approach challenges with confidence, make informed decisions, and adapt to new situations in both my professional and personal endeavors.
