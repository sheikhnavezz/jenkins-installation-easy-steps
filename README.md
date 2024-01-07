# Jenkins-installation-easy-step
## Installing Jenkins on Ubuntu

### Step 1: Launch an instance in aws with (AMI: ubuntu, instance type: t2.medium)

![1 instance_img](https://github.com/sheikhnavezz/jenkins-installation-easy-steps/assets/134357661/02ae0a25-46ff-4eac-990c-5b7ec504f717)

### Step 2: SSh (mobaxterm or any terminal cmd: ssh -i <your keyname> ubuntu@public ip)

![2 ssh](https://github.com/sheikhnavezz/jenkins-installation-easy-steps/assets/134357661/d1431aa2-d31f-4393-86cf-6d17727cf95a)

### Step 3: sudo su -----(root login)

### Step 4: apt update -y -----first update the server

![3update_instance](https://github.com/sheikhnavezz/jenkins-installation-easy-steps/assets/134357661/83a01414-8d5d-44d8-9e0d-ca6b56462e96)

### Step 5: apt install fontconfig openjdk-17-jre -y  ----install java

### Step 6:  Installing Jenkins 

sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key

echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt-get update

sudo apt-get install jenkins -y 

![4 jenkins_installation](https://github.com/sheikhnavezz/jenkins-installation-easy-steps/assets/134357661/34363430-f57f-4438-b330-aea2515cdeb1)

### Step 7: Goto aws console EC2 service

### Step 8: Add inbound rule in security group as (all traffic and anywhere ipv4)

### Step 9: copy public ip and paste in browser with port no. (<public ip:8080>)  ---you will see the jenkins page 

![5 sg](https://github.com/sheikhnavezz/jenkins-installation-easy-steps/assets/134357661/ad551beb-1396-47cb-862d-4b7ebf30f275)

### Step 10: now, copy the path from there starting from (/var/lib)

![6 jenkins_page](https://github.com/sheikhnavezz/jenkins-installation-easy-steps/assets/134357661/5bc43565-a162-43b9-a85d-995611707880)

### Step 11: then goto terminal paste that path with <cat cmd> as (cat /var/lib/jenkins/secrets/initialAdminPassword)

![7 cmd](https://github.com/sheikhnavezz/jenkins-installation-easy-steps/assets/134357661/2b514b38-d76e-4c84-a81c-1b07ebf8529f)

### Step 12: you will get the password copy and paste in the admin. password which is in browser jenkins page. 

![8 admin_pass](https://github.com/sheikhnavezz/jenkins-installation-easy-steps/assets/134357661/185a0b79-0e40-4d6c-924f-cb8a7acd4e88)

### Step 13: customize jenkins (click) on install suggested plugins 

![9 getting_started](https://github.com/sheikhnavezz/jenkins-installation-easy-steps/assets/134357661/0dc8b302-7132-4e5e-b9a6-08635342d84f)

### Step 14: give credentials: user1 > pass: 12345
confirm pass: 12345 > fullname: admin : email: admin@gmail.com > (click) save and continue > save and finish > (click) star using jenkins 

![10 user_cred](https://github.com/sheikhnavezz/jenkins-installation-easy-steps/assets/134357661/6aa69b0f-5233-46a8-a37b-783bfe1125e3)

### Step 15: Now, (click) save and continue

### Step: 16: Then, (click) Start using jenkins.

![11 start_jenkins](https://github.com/sheikhnavezz/jenkins-installation-easy-steps/assets/134357661/d26837a5-da51-492f-95b9-2025f5c7f0a7)

### There you will see the Jenkins dashboard..!

![12 jenkins_dashboard](https://github.com/sheikhnavezz/jenkins-installation-easy-steps/assets/134357661/18fb144d-e887-4405-b403-ab8f60f5743a)


                                ## Hence, You have successfully installed jenkins on your ubuntu server.
