
##sDeploy Spring Boot application on ec2 Instance.

EC instance type: use Amazon Linux 2 AMI (HVM),


This application will demonstrate running of Spring boot simple Hello world application
on Ec2 instance.

1. Create Ec2 instance manually from aws console.
use AWS Linux 2


2. Install Jdk 8 on newly launched Ec2 instance.
sudo su

yum update -y
sudo yum -y install java-1.8.0

3. check for java -version

4. Create a spring boot Helloworld project using spring intializer
Add controller class to have the response for Helloworld

4.1  mvn clean package

5. Upload the  jar to s3 bucket 

6. download the jar file from s3 to ec2 instance

wget https://haider0808.s3.amazonaws.com/helloworld-0.0.2.jar

7. start the jar file using 

java - jar helloworld-0.0.2.jar

The port application listens on port 8082 so make sure to enable port 8082 for inbound traffic.


Test the url through

http://<public-ip>:8082/api/v1.greeting
