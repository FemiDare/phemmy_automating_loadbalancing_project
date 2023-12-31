# phemmy_automating_loadbalancing_project

I spun two EC2 instances on AWS namely "first apache" and "second apache" making sure to open port 8000 by adding a new inbound rule so as to serve content through that port

I then opened two terminal windows and connected to the two EC2 instances via ssh after which I changed each hostname to "firstapache" and "secondapache" respectively and then updated both systems

![Screenshot 2023-11-06 211251](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/2183d3f5-35b0-4471-8fd3-4e9f78e420cd)

![Screenshot 2023-11-06 211419](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/b14995a5-de7b-465c-adbc-23c35f239a81)

![Screenshot 2023-11-06 211629](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/d2a408f2-d5a3-4ca1-a264-bfccfead1abc)

![Screenshot 2023-11-06 211734](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/a066c016-04f3-47bf-be11-5fdc03e854eb)

![Screenshot 2023-11-06 212153](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/c107490c-9061-4728-acc5-f27772f25772)

![Screenshot 2023-11-06 212305](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/554e2ea2-f7cd-4759-8f80-83eb6fb0001d)

![Screenshot 2023-11-06 212422](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/2fb3cbe2-12a6-4c39-976b-efce532b2348)

![Screenshot 2023-11-06 212506](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/19cf5a70-6f91-4c44-b70e-211278d1f386)

I then opened a script file named "install.sh" on both systems using the vi command and pasted the provided script inside both files. 

The purpose of the script files being to automatically update my system and install apache webservers and check the status to check/confirm that they are running/active and restart the apache web servers

After that I changed the permissions on the script files so as to make them executeable and then ran the script files making sure to input the respective public IPs as specified in the scripts

I then ran both public IPs on my web browser to verify that the scripts ran as intended

![Screenshot 2023-11-06 212716](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/4277c8e0-8b07-42e4-a5f0-a270938db8d1)

![Screenshot 2023-11-06 213115](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/3a94aa88-8cb4-4e2a-a0a0-72c4bc0f3d25)

![Screenshot 2023-11-06 213221](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/b254df11-211e-4a0d-95e3-b6e21e33e65b)

![Screenshot 2023-11-06 213326](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/ded2af19-87e1-4113-89ca-11a47e7b5f5d)

![Screenshot 2023-11-06 213420](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/c874a5a0-4f84-4e31-94f9-55f497907f62)

![Screenshot 2023-11-06 213528](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/7fc228c3-faaa-46c9-82aa-e01abb441816)

![Screenshot 2023-11-06 213631](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/47caba38-500a-4094-9522-9869202cbe30)

![Screenshot 2023-11-06 213708](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/2710a22a-b9b2-4317-bb62-92bb13a674fa)

![Screenshot 2023-11-06 213744](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/acd262ea-652c-420b-9da6-49fde641b92b)

![Screenshot 2023-11-06 213833](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/18b9b0ce-06ae-4912-b542-38cb98c2367b)

![Screenshot 2023-11-06 213919](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/c6eac6de-e0e9-4478-9d77-14ef0c394cef)

![Screenshot 2023-11-06 214319](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/5e517213-edcf-41f3-a424-242dd78ce113)

I then launched a new EC2 instance named "nginx loadbal" and made sure to open port 80 by adding a new inbound rule so as to serve content through that port

I then opened a new terminal window and connected to the EC2 instance via ssh after which I changed the hostname to "nginxbalancer" and then updated the system

![Screenshot 2023-11-06 215028](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/be2d09b5-4706-493c-94fe-45ea21eaa9d8)

![Screenshot 2023-11-06 220454](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/b75a4e43-5593-4a02-973f-0259c66ea813)

![Screenshot 2023-11-06 215525](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/661cc6b4-e1fd-4371-b64b-20deb97e6122)

![Screenshot 2023-11-06 215622](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/db1f14d3-3223-46d2-8c4c-ee448d72011b)

I then opened a script file named "nginx.sh" on this system using the vi command and pasted the provided script inside the file.

The purpose of this script file being to automatically configure nginx as a load balancer for the previous two apache webservers created and test that in was configured properly and then restart the nginx server

After that I changed the permission on the script file so as to make it executeable and then ran the script file making sure to input the respective public IPs as specified in the scripts

I then moved to my web browser to test using the nginx public IP and refreshing to verify that it was switching between both apache web servers

![Screenshot 2023-11-06 215742](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/fcfaf6a5-bc0c-40b8-b379-19d8f1fdbd73)

![Screenshot 2023-11-06 215846](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/6857baa8-118b-4a9a-8ad3-ffbe5e34b326)

![Screenshot 2023-11-06 215931](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/de17ba23-e5b4-418f-b5bf-e784d294775b)

![Screenshot 2023-11-06 220144](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/b4f07191-cf4c-44b3-a571-4595fc97e73e)

![Screenshot 2023-11-06 220230](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/44d08c52-ade3-46fc-a22a-d56d3ff52b96)

![Screenshot 2023-11-06 220532](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/3524e3ec-6a97-4871-8f85-551888a7d9ee)

![Screenshot 2023-11-06 220553](https://github.com/FemiDare/phemmy_automating_loadbalancing_project/assets/140294606/a0dfdcdf-baa5-4e9a-8623-9200f4caa98a)
