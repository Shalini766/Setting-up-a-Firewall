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

## Configuring Firewall Rules to Allow and Block Specific Traffic

UFW allows you to add specific rules for blocking or allowing traffic based on ports, IP addresses, and protocols.

### Allowing a Specific Port: 

To allow a specific port (e.g., port 8080): *sudo ufw allow 8080*

![image](https://github.com/user-attachments/assets/4d183479-8079-4593-a5af-3cebde3e24a6)

To specify protocol: TCP or UDP, use: *sudo ufw allow 8080/tcp*

![image](https://github.com/user-attachments/assets/c2282ab1-bbfa-4df5-8ccc-4353e6c27632)

### Blocking a Specific Port: 

To block a specific port (e.g., port 8080): *sudo ufw deny 8080*

![image](https://github.com/user-attachments/assets/c3ea3d25-b37a-4945-88bb-f1590e94607e)


### Allowing or Blocking Specific IP Addresses:

To allow traffic from a specific IP address (e.g., 192.168.1.100): *sudo ufw allow from 192.168.1.100*

![image](https://github.com/user-attachments/assets/be1846d6-ebf2-4bc5-8c95-baef0771879e)


To block traffic from a specific IP address: *sudo ufw deny from 192.168.1.100*

![image](https://github.com/user-attachments/assets/f51f852d-2512-4a65-bf71-1308dac0daa2)


### Allowing or Blocking a Specific IP Address on a Specific Port: 

For example, to allow IP 192.168.1.100 to access port 80: *sudo ufw allow from 192.168.1.100 to any port 80*

To block the same IP from accessing port 80: *sudo ufw deny from 192.168.1.100 to any port 80*

![image](https://github.com/user-attachments/assets/22cad3bd-4984-4070-9a6e-065e3be99ab4)

### Allowing Specific IP Ranges:

You can also allow or block IP address ranges: *sudo ufw allow from 192.168.1.0/24*

![image](https://github.com/user-attachments/assets/ddedd76b-5c86-4780-b4dc-b1b0e5fa9faa)


### Allowing or Blocking a Range of Ports: 

For example, to allow ports 1000 to 2000: *sudo ufw allow 1000:2000/tcp*

![image](https://github.com/user-attachments/assets/b9717451-31d4-4f08-a2a6-93a0e1bccb68)


My firewall status after management

![image](https://github.com/user-attachments/assets/2979360a-0a07-4da8-bab8-9abc5a8d219a)

## Advanced Firewall Configuration with UFW


**Logging**: UFW supports logging, which helps track firewall activity. 

You can enable logging with: *sudo ufw logging on*

![image](https://github.com/user-attachments/assets/14c65b2f-4322-4064-a236-354e4e49008c)

 
By default, logs are saved to /var/log/ufw.log.

**Rate Limiting**: Protect services from brute-force attacks by limiting the rate of incoming connections.

For example, to limit SSH connections to 3 attempts per minute: *sudo ufw limit ssh*

![image](https://github.com/user-attachments/assets/de1cdc0f-534b-4fe9-a886-cd99af51e164)






