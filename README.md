Steps to create docker image from Java application
Step1:
First create one instance in Google cloud.

 

Step2:
Open the browser from GCP 

 

Then go to sudo user:
 





Once successfully connect the instance then do the update
command: yum update -y 
Step5:Install the docker in GCP
command: yum install docker -y
Step6:check the docker running status. Below its showing running.
  service docker status 

 

Step8:Install git in this machine because we need to clone project and create the image,push in to docker hub
command: yum install git
Step9: Take my code and do the clone,

git clone https://github.com/RameshEY/RameshEY.git

 




Step10:Check the docker file inside this project. 

 

Step11:Create docker image

docker build -t learning-demo .

 

Step12:check the images

 

Push the Image:
Step1:
First create the account in the docker hub(dockerhub.com)
Step2:
 Already created
-->Docker Id:_______
-->Docker user name:-----Email id
-->Chose password
Step3:

docker tag learning-demo username/learning-demo
Exam:docker tag learning-demo testdockerramesh/learning-demo

 

Step4:
login in to docker hub
docker login --username <> --password ****
 
push the image:
docker push testdockerramesh/learning-demo
 

Sceen shot:

 

Pull the image:
Create another machine. Install the docker and pull the image.

docker pull testdockerramesh/learning-demo

Run the container:

docker run -d -p 8054:8054 testdockerramesh/learning-demo

 




After run the container then go to firewall allow the port as 8054

 

 

Check the application access from out side:

 


