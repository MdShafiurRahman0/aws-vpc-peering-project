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



Step 4: Update VPC 1's route table

1. Select the checkbox next to VPC 1's route table i.e. called NextWork-1-rtb-public.
2. Scroll down and click on the Routes tab.
3. Click Edit routes.
4. Let's add a new route!
5. Add a new route to VPC 2 by entering the CIDR block as our Destination  10.2.0.0/16.
6. Under Target, select Peering Connection.
7. Select VPC 1 <> VPC 2.
8. Click Save changes.


![image](https://github.com/user-attachments/assets/1aa91e03-1a46-4591-bb78-486b881e9456)

![image](https://github.com/user-attachments/assets/26006285-39f2-4b00-b56d-2a53ad8fb8b2)



Step 5: Update VPC 2's route table

Challenge yourself - do you think you can set up the equivalent route in VPC 2's route table?


1. The route table you're updating is -2-rtb-public.
2. The Destination is the CIDR block 10.1.0.0/16.


![image](https://github.com/user-attachments/assets/2c10d289-58bf-4f30-9af1-7c5f0e58934f)


Step 6: Launch EC2 Instances


![image](https://github.com/user-attachments/assets/67e9101d-d63c-4620-8eec-99ddad041742)

1. Head to the EC2 console - search for in the search bar at the top of screen.
2. Select Instances at the left hand navigation bar.
3. Select Launch instances.
4. Since your first EC2 instance will be launched in your first VPC, let's name it 
5. For the Amazon Machine Image, select Amazon Linux 2023 AMI.
6. For the Instance type, select t2.micro.
7. For the Key pair (login) panel, select  Proceed without a key pair (not)

![image](https://github.com/user-attachments/assets/ccd83b75-9bf1-47b1-885e-127e16ae312d)



8. Under VPC, select vpc-1.
9. Under Subnet, select your VPC's public subnet.
10. Keep the Auto-assign public IP setting to Disable.
11. For the Firewall (security groups) setting, Amazon VPC already created a security group for your VPC - let's use that!
12. Choose Select existing security group.
13. Select the default security group for your VPC.

![image](https://github.com/user-attachments/assets/04922c77-09b5-4d52-a4c9-23bd3951764d)


Step 7: Launch an instance in VPC 2

## Same as Previous Steps

![image](https://github.com/user-attachments/assets/b13a5209-d086-4a5c-b3d2-9db1e349d1ca)
