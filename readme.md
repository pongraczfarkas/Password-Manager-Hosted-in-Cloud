# Password Management System in AWS

## Description

This guide explains how I set up a self-hosted password manager environment using Passbolt on AWS. The purpose of this project was to gain experience with secure password management, learning how to implement, configure, and maintain a robust system for safeguarding sensitive data. This project highlights key steps in deploying and managing a secure, cloud-based application. Using Passbolt hosted on AWS, I will ensure secure storage of complex passwords.

## Environments used

- Oracle VM VirtualBox
- Ubuntu 24.04
- AWS EC2

## Links

- Passbolt: [Deploy Passbolt to AWS](https://www.passbolt.com/ce/aws)
- Oracle VM VirtualBox: [Download](https://www.virtualbox.org/wiki/Downloads)
- Ubuntu: [Download](https://ubuntu.com/download/desktop)

## Walkthrough

First, I headed to the Passbolt link and then clicked on the yellow "Deploy to AWS" button.
<p align="center">
  <img src="https://github.com/user-attachments/assets/b1365bc7-b010-4306-9f4e-155a57c4f974" alt="Deploy to AWS button">
</p>

On the next screen, I clicked "Continue to Subscribe" to agree to the terms and proceed with the subscription.
<p align="center">
  <img src="https://github.com/user-attachments/assets/40cffb5f-f1ec-4562-84dc-47f73b9f1f5b" alt="Continue to Subscribe">
</p>

Next, I started configuring my instance in AWS by clicking "Continue to configuration".
<p align="center">
  <img src="https://github.com/user-attachments/assets/3b5deb26-8490-4237-b983-78df63fe9f87" alt="Continue to configuration">
</p>

I selected the most optimal server for running this EC2 instance. I kept the default settings for the rest of the options.
<p align="center">
  <img src="https://github.com/user-attachments/assets/9d13d30d-674f-4dcf-94a2-c96c5ec2cfd1" alt="Server selection">
</p>

On the next page, I left all the settings as default, except for the security group settings, where I used Passbolt's recommended configuration to ensure proper security measures.
<p align="center">
  <img src="https://github.com/user-attachments/assets/f5892f7a-7179-44c2-9ddc-2bb506692309" alt="Security group settings">
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/366d5214-9557-4cb1-addc-370df9e55840" alt="Security group settings continued">
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/79e75ec3-9dca-47ab-b0bb-81fe338c15f6" alt="Security group settings final">
</p>

I then generated a public key using my Ubuntu VM and entered it here.
<p align="center">
  <img src="https://github.com/user-attachments/assets/df1b3c1a-af61-47df-b874-bdb65163a59d" alt="Public key input">
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/a5861569-e7c3-48c6-b266-bc21c53c0c60" alt="Public key input confirmation">
</p>

After entering the public key, I clicked "Launch" to start the instance.
<p align="center">
  <img src="https://github.com/user-attachments/assets/00b8f1bb-9947-49f8-8150-4c6db13fa881" alt="Launch instance">
</p>

With the instance launched, I navigated to the AWS Dashboard to find the IP address of the instance. This IP address is necessary for configuring Passbolt.
<p align="center">
  <img src="https://github.com/user-attachments/assets/da043610-415c-42cd-af6c-3536e1aad92d" alt="AWS Dashboard">
</p>

Upon reaching the starting screen, I began the setup process for Passbolt. Although using an SSL certificate would make the site more secure and allow HTTPS configuration, I chose to skip this for simplicity.
<p align="center">
  <img src="https://github.com/user-attachments/assets/f105e22b-7957-4086-ab8e-f60d927e4994" alt="Passbolt start screen">
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/3f5b9176-af34-498c-8591-c2aa42675f4d" alt="Skip SSL">
</p>

I kept all other settings as default.
<p align="center">
  <img src="https://github.com/user-attachments/assets/7538f2c2-a1e9-4a93-86d2-4a22796c4b08" alt="Default settings">
</p>

Since I was setting up a temporary environment, I supplied some placeholder information.
<p align="center">
  <img src="https://github.com/user-attachments/assets/f6be1c71-609d-43a9-b7b0-c173fc882964" alt="Placeholder information">
</p>

Again, I left everything as default.
<p align="center">
  <img src="https://github.com/user-attachments/assets/5088a5ae-9c31-45b6-9459-2b45daf4826c" alt="Default settings confirmation">
</p>

The next step involved configuring the SMTP server, which is necessary for email notifications.
<p align="center">
  <img src="https://github.com/user-attachments/assets/46396094-d5dc-47fc-8106-e87df334b6b7" alt="SMTP configuration">
</p>

I then created my user account on Passbolt.
<p align="center">
  <img src="https://github.com/user-attachments/assets/f8a93045-c89c-4667-bad2-d993c6773624" alt="User account creation">
</p>

Passbolt required me to install a Firefox browser extension, a mandatory step for secure password management.
<p align="center">
  <img src="https://github.com/user-attachments/assets/f311f092-6b88-4a8e-8e44-bec7cbce564e" alt="Firefox extension installation">
</p>

After installing the extension, I provided my passphrase. This is the only password I need to remember to access all my stored passwords.
<p align="center">
  <img src="https://github.com/user-attachments/assets/5f4a8362-ab54-4a43-9cc5-2ec5e23fa5d9" alt="Passphrase input">
</p>

Passbolt then automatically downloaded my recovery kit to my PC and displayed a security token to personalize. This step helps prevent phishing attacks.
<p align="center">
  <img src="https://github.com/user-attachments/assets/9810c341-be9b-442b-b275-bca27d309f60" alt="Recovery kit and security token">
</p>

Finally, my password manager setup was complete.
<p align="center">
  <img src="https://github.com/user-attachments/assets/1620e8db-4fd0-44e8-b605-b1e2da0227c9" alt="Passbolt setup complete">
</p>


















