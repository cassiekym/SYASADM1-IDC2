![image](https://github.com/user-attachments/assets/f57c8e4f-62a7-4d5e-b486-08f81ee41cde)

# SYSADM1 – Kerberos Lab Activity: A step-by-step Guide

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

![image](https://github.com/user-attachments/assets/8f4b0be1-886b-46b7-b2c8-120a2ed899e6)

2. **Install Kerberos Server Packages on VM1 (Kerberos Server):**

   * In VM1, install the Kerberos Key Distribution Center (KDC) and admin server:

*bash*

*sudo apt install krb5-kdc krb5-admin-server –y*

![image](https://github.com/user-attachments/assets/8d2189fe-b50c-4b01-b182-18bc966d8db8)

3. **Install Kerberos Client Package on VM2 (Kerberos Client):**

   * In VM2, install the Kerberos client software:

*bash*

*sudo apt install krb5-user –y*

![image](https://github.com/user-attachments/assets/657876ba-8aa2-40e6-b592-0e0fb1a0be11)

* During installation, when prompted, enter the Kerberos realm you plan to set up, e.g., MYLAB.LOCAL.

![image](https://github.com/user-attachments/assets/32d74a4c-8e66-48a6-8cdf-8945bd9c3d20)

**Step 2: Configure the Kerberos Server (VM1)**

1. **Edit the Kerberos Configuration File:**

   * Open /etc/krb5.conf for editing:

*bash*

*sudo nano /etc/krb5.conf*

![image](https://github.com/user-attachments/assets/2b0ca757-14bd-4c39-a71d-b8afa3fcd8bb)

* Set the realm as MYLAB.LOCAL. You should also specify the KDC and admin server as VM1’s hostname or IP address:

ini

\[libdefaults\]

    default\_realm \= MYLAB.LOCAL

\[realms\]

    MYLAB.LOCAL \= {

        kdc \= \<VM1\_IP\_or\_hostname\>

        admin\_server \= \<VM1\_IP\_or\_hostname\>

    }

* Save and close the file (Ctrl+X, then Y, and Enter to confirm).

![image](https://github.com/user-attachments/assets/26ce4dd1-9213-4eb1-aa48-a73aae5f3ada)

2. **Initialize the Kerberos Database:**

   * Create the database for the Kerberos realm:

*bash*

*sudo krb5\_newrealm*

* You will be prompted to set a password for the Kerberos database.

![image](https://github.com/user-attachments/assets/7f2b8fe5-a685-4b19-89f7-ec18c8d4f688)

3. **Start and Enable the Kerberos Services:**

   * Start the KDC and admin server, and ensure they start automatically on boot:

*bash*

*sudo systemctl start krb5-kdc*

*sudo systemctl start krb5-admin-server*

*sudo systemctl enable krb5-kdc*

*sudo systemctl enable krb5-admin-server*

![image](https://github.com/user-attachments/assets/736b8ce5-e451-4996-8e8e-5c738c64dfab)

**Step 3: Set Up a Kerberos User Principal**

1. **Create a New User Principal:**

   * Run the following command to create a test user in the Kerberos realm:

*bash*

*sudo kadmin.local \-q "addprinc testuser@MYLAB.LOCAL"*

* Set a password for testuser.

![image](https://github.com/user-attachments/assets/296f7bb1-af29-48dd-a580-2fa04cba324f)

2. **Verify the User Principal:**

   * To confirm the principal is created, list all principals:

*bash*

*sudo kadmin.local \-q "listprincs"*

![image](https://github.com/user-attachments/assets/3ccb534a-1122-4fe5-9959-d1ecca73fe79)

**Step 4: Configure the Kerberos Client (VM2)**

1. **Edit the Kerberos Configuration File on VM2:**

   * Open /etc/krb5.conf for editing on VM2:

*bash*

*sudo nano /etc/krb5.conf*

* Set the default realm to MYLAB.LOCAL and point to the KDC and admin server on VM1. The configuration should match what you set on VM1.

![image](https://github.com/user-attachments/assets/abac527b-2b05-4ec1-b4b8-263b2acce2e9)

**Step 5: Test Kerberos Authentication**

1. **Request a Kerberos Ticket for the User on VM2:**

   * In the terminal on VM2, request a ticket for testuser:

*bash*

*kinit testuser@MYLAB.LOCAL*

* Enter the password you set for testuser.

![image](https://github.com/user-attachments/assets/5d0492d7-0c4e-4fc6-8f3e-f85432da249a)

2. **Verify the Ticket:**

   * Check if the ticket was issued by listing active Kerberos tickets:

*bash*

*klist*

* You should see details about the ticket, such as the principal and expiration time, confirming successful Kerberos authentication.

![image](https://github.com/user-attachments/assets/572511d1-5a41-4068-a8a7-539db658350b)
