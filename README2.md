step1: we have fork this reposity from LondheShubham153 

![image](https://user-images.githubusercontent.com/120701020/233610310-54d46724-dd63-4cde-9c45-d21d389c2f7e.png)

Step2: In Jenkins select GitHub project and copy the fork repository URL like this

![image](https://user-images.githubusercontent.com/120701020/233610573-56630ec2-89b5-45af-b81f-f035767f5d04.png)

Then paste it in Jenkins GitHub project section like this

![image](https://user-images.githubusercontent.com/120701020/233610744-c4157aa9-a87c-47de-9c82-0cfdbc2564c3.png)

Step 4: In the Source Code Management select Git and copy the repository HTTP URL like this

![image](https://user-images.githubusercontent.com/120701020/233610842-ab248b9e-c4b4-4a58-a38a-4faf3ebd5be6.png)

and paste it in the Source Code Management section and set the Branch Specifier to master like this and you no need add credentials here because it public repository.

![image](https://user-images.githubusercontent.com/120701020/233610924-3f7715f7-e058-4b90-adef-a50417c119de.png)

step 5: You need to install docker-compose in the server

sudo apt-get install docker-compose

![image](https://user-images.githubusercontent.com/120701020/233612185-9bbfb482-e46e-49f7-911d-e21d76ce112d.png)

Step 6: Give permission to Jenkins and reboot the server and reboot your Jenkins as well like this

![image](https://user-images.githubusercontent.com/120701020/233612258-8ca2684d-42ed-4c54-a5bf-4d15d414e44e.png)

![image](https://user-images.githubusercontent.com/120701020/233612320-6085e204-63e7-42c8-b468-8f710547f047.png)


Step 7: In the Build steps run these commands and click save

docker-compose down

docker-compose up -d

![image](https://user-images.githubusercontent.com/120701020/233611443-0a608842-42be-4923-b38c-ba5f843ba914.png)

Step 8: In instance, security group add 8000 port because we have added port 8000 in docker-compose.ymal file

![image](https://user-images.githubusercontent.com/120701020/233612884-40116381-860f-4766-9fef-37e6651b5eb4.png)

![image](https://user-images.githubusercontent.com/120701020/233612938-add242e5-2e95-4771-b3b5-1b2dd923da55.png)

Step 9: Now click on Build now

![image](https://user-images.githubusercontent.com/120701020/233613003-3106006d-7b81-4810-9989-3d8eb68cbbea.png)

you can see its running and click on it

![image](https://user-images.githubusercontent.com/120701020/233613069-f10e44a8-c975-4b00-9e8d-289f1f3db2bb.png)

and go to console output you see this

![image](https://user-images.githubusercontent.com/120701020/233613141-a2fe3060-c16d-4e92-9018-193d98c405f5.png)

Step 10: Now go to instance IP address

![image](https://user-images.githubusercontent.com/120701020/233613224-ce8acc6b-226d-42b2-b914-7f5b2eba11ea.png)

Copy and paste it into google chrome and add ":8000" at the end of the IP address to it like this

![image](https://user-images.githubusercontent.com/120701020/233613295-9a54329c-03c7-409d-94a2-98a403175f4e.png)

Now you see this page and also we have completed our task 02 as well which deploy the node todo app through docker-compose in Jenkins

![image](https://user-images.githubusercontent.com/120701020/233613376-113393df-84fa-4fe2-9cb5-8f3057f21fcc.png)
