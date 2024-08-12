# AWS VPC Peering Project

## Get ready to:

☁️ Set up multiple VPCs.
🌉 Create a VPC peering connection - i.e. get two VPCs to talk to each other!
👩‍🔬 Test VPC peering with connectivity tests.


# High Level Overview Architecture 
![image](https://github.com/user-attachments/assets/257f282e-cf85-4daf-a88c-0c6f2be9e391)


# Step 1: Set up VPCs in Minutes

1. Create two VPCs from scratch!
2. Use the visual VPC resource map to create your VPCs supa fast 😎⚡️

![image](https://github.com/user-attachments/assets/ebbf067d-2c80-43ec-9bbd-e3ed4bb0c55d)

![image](https://github.com/user-attachments/assets/9034b352-3d2a-4b2f-972c-65d70c8e161e)


3.  The VPC's IPv4 CIDR block is must be 10.1.0.0/16.





![image](https://github.com/user-attachments/assets/ef54d069-1c40-487b-bf68-01188eb357a4)


4.  Next, for the NAT gateways ($) option, make sure you've selected None. As the dollar sign suggests, NAT gateways cost money!


![image](https://github.com/user-attachments/assets/c3b1758b-5ee0-4ebe-a66f-f8444f705d95)

![image](https://github.com/user-attachments/assets/c0bebd3a-59e7-43be-a5f2-e67b7c5ceec1)

![image](https://github.com/user-attachments/assets/4088ea6a-2678-427e-b064-48c3ae689b0f)



Step 2: Set up VPC 2 

1. For IPv6 CIDR block, we'll leave in the default option of No IPv6 CIDR block.
2. For Tenancy, we'll keep the selection of Default.
3. For Number of Availability Zones (AZs), we'll use just 1 Availability Zone.
4. Make sure the Number of public subnets chosen is 1.
5. For Number of private subnets, we'll go with 0 for today's project. Let's keep it simple with just a single subnet!
6. For the NAT gateways ($) option, select None. 
7. For the VPC endpoints option, select None.
8. You can leave the DNS options checked.
9. Select Create VPC.


Step 3: Create a Peering Connection

![image](https://github.com/user-attachments/assets/cd2d9ac5-e511-4f89-915c-44f3f9b5448a)

1. Click on Create peering connection in the right hand corner.

![image](https://github.com/user-attachments/assets/99de1dfd-6c47-40b1-855a-8c7b0d608dcb)


![image](https://github.com/user-attachments/assets/6bc0a630-1326-4be2-b1fd-8ba36eb7fb2a)

![image](https://github.com/user-attachments/assets/cd5213a1-cdda-4ed8-932e-c2cc232f3771)

![image](https://github.com/user-attachments/assets/f1e289e6-b334-45ae-9f76-565a288999a1)


![image](https://github.com/user-attachments/assets/db87c92d-632c-4ffd-854c-291417b25721)



1. Click on Accept request again on the pop up panel.
2. Click on Modify my route tables now on the top right corner.

![image](https://github.com/user-attachments/assets/00f1c962-0711-4e3f-bf6d-1b6b3b92ef14)
