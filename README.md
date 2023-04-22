# CC3_403_411_416_418
CC Project- Problem Statement 3

The code can be viewed in the main branch!

Problem Statement: Deployment of Web App Using AWS Cloud

Description of Solution:
We first created an AWS EC2 instance in a public subnet, and then created and then created RDS database in a private subnet hosted on the cloud. We then connected the EC2 instance to the RDS database. Security group ec2-rds-x is created and added to the EC2 instance. It has one outbound rule that references the rds-ec2-x security group as its destination. Security group rds-ec2-x is created and added to the RDS database. It has one inbound rule that references the ec2-rds-x security group as its source. The RDS database uses MySQL. The database name is hospital_db.

1.View of the dashboard

![Screenshot (1045)](https://user-images.githubusercontent.com/78139587/233398896-2a2e5788-a0cd-4764-8c3b-6b09ba56f90b.png)


2.Add/Create doctor and view on the dashboard

![Screenshot (1046)](https://user-images.githubusercontent.com/78139587/233398988-278e3310-d949-4a8d-a9c2-109ba49a2ad7.png)

![Screenshot (1047)](https://user-images.githubusercontent.com/78139587/233399002-65ad8a92-aa79-4efa-b4a7-8ee2a381eb82.png)


3.View on the console

![Screenshot (1048)](https://user-images.githubusercontent.com/78139587/233399022-070ecaff-64d2-4bbc-90a9-4bc38d0660db.png)

4.Update doctor and view on the dashboard

![Screenshot (1049)](https://user-images.githubusercontent.com/78139587/233399054-bc422935-7543-474f-9345-6c7c5027f824.png)

![Screenshot (1050)](https://user-images.githubusercontent.com/78139587/233399087-48dcfd33-c332-4daf-b182-37ea2b987377.png)

It can be seen above that the update being made is the specialization of doctor "Shruthi" from Ortho to Gynaecologist


5.View on the console

![Screenshot (1051)](https://user-images.githubusercontent.com/78139587/233399114-86645725-98fc-4795-a097-ca014e612015.png)


6.Delete doctor and view update on the dashboard

![Screenshot (1052)](https://user-images.githubusercontent.com/78139587/233399139-3b19d160-c1cc-4dd3-838f-4b278f4f1462.png)

![Screenshot (1053)](https://user-images.githubusercontent.com/78139587/233399162-93095a98-c238-4d67-8d3d-80caf52509cc.png)

It can be seen above that the doctor being deleted is "Shruthi"


7.View on the console
![Screenshot (1054)](https://user-images.githubusercontent.com/78139587/233402097-c45ed848-5325-4563-ae6e-0e4a8103de5d.png)



Important commands used:

1. To connect and login to sql, the command used is: mysql -h database-cc.crarwjcqa1fg.us-east-1.rds.amazonaws.com -u admin -p   
2. To move file from local system to ec2 instance, the command used is: scp -i newkey.pem medibed.zip root@ip-172-31-94-47:~/
3. To move file from ec2 instance to the local system, the command used is: scp -i newkey.pem ec2-user@ec2-44-210-130-126.compute-1.amazonaws.com:/var/www/html/doctor/* .
4. The url to view the webpage is: http://18.207.196.99/master.php

The below image is of the ec2 instance:

![image](https://user-images.githubusercontent.com/78139587/233401211-5ed53027-8a3a-4266-8b9e-52dd2e705f10.png)


The below image is of the RDS database:

![image](https://user-images.githubusercontent.com/78139587/233401131-05ade6e2-49cd-472a-840a-a1a04f983f19.png)



