# Setting-up-a-Firewall
Firewalls play an essential role in network security by ensuring only authorised access.

The project explores the process of setting up and configuring a basic firewall on a virtual machine (VM) using UFW (Uncomplicated Firewall) demonstrating the step-by-step process of enabling the firewall, configuring rules to allow or block specific types of traffic, and verifying the rules using various commands. 

From this project users can gain hands-on experience in securing a virtual machine by effectively using firewall rules to control inbound and outbound traffic. The ultimate goal is to enhance system security by preventing unauthorized access while ensuring legitimate traffic flows seamlessly.

## Requirements:
- A Linux-based VM (Kali Linux).
- Access to the terminal with root or sudo privileges.

## Steps

### Step 1: Installing UFW
-Open the terminal and run the following command to install UFW

    *sudo apt-get update*
    *sudo apt-get install ufw*

![image](https://github.com/user-attachments/assets/e36b3c73-f240-4779-8643-2958fc7b7e1c)

### Step 2: 2.	Enabling the UFW Firewall

Run the following command to enable the firewall

*sudo ufw enable*

![image](https://github.com/user-attachments/assets/7338a911-883f-4ab6-ab41-5e20548c69df)

### Step 3: Check the UFW Status

Run the following command to check the status of the firewall

*sudo ufw status verbose*

![image](https://github.com/user-attachments/assets/182337d7-96d1-4f6c-969f-ca094bd90ff8)

### Step 4: Allow SSH Connections

Allow SSH connections in the firewall.

*sudo ufw allow ssh*

![image](https://github.com/user-attachments/assets/37603753-13a9-4519-8007-bec2f6647391)

### Step 5:Allowing and Blocking Traffic by Default

This step includes blocking incoming traffic and allowing all outgoing traffic through the firewall.


*sudo ufw default deny incoming*

*sudo ufw default allow outgoing*

![image](https://github.com/user-attachments/assets/32af60ea-a78b-4f2e-8fc6-e6a826dc5e20)

![image](https://github.com/user-attachments/assets/da545ea8-be00-4eb3-a1c4-eb8aa2bba68c)

### Step 6: 6.	Allow HTTP and HTTPS Traffic

*sudo ufw allow http*

*sudo ufw allow https*

![image](https://github.com/user-attachments/assets/f77707fc-9f2a-479e-9845-3bec0e6a441c)

![image](https://github.com/user-attachments/assets/b0fd8a73-1d93-4ec8-ba80-55700ae37a74)

### Step 7: Verify the Firewall Rules

*sudo ufw status*

![image](https://github.com/user-attachments/assets/1fa85fb6-78b6-4d1d-87ee-bb78388e1312)












