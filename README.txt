Name: James Yu
Student ID: 101057704
Project: Movie Database

OpenStack Instance Information
---------------------------------
Public IP Address:134.117.132.194
Username:student	
Password:101057704

Source Files: 
In the main folder is server.js
In the data folder is movie-datajson, movie-data-short.json and users.json files
Lastly, in the views folder is my pages and partials; header.pug, footer.pug and in the pages sub-folder is 21 pug files.

Connect to Openstack Instance:
First, make sure that you are connected to the schoolvpn through CISCO. Once you are, open up windows powershell and type in the following command: "ssh student@134.117.132.194". It will then prompt you to enter if you wish to continue connecting, type "yes" and hit enter. It will then prompt you for a password which is "101057704". 

****IMPORTANT NOTE****: I was having issues with EADDRINUSE issues on openstacks so it might be a good idea to kill all system processes using 
"killall -9 node"

How to Initialize and run server on OpenStack Instance:
Once you have successfully connected to the instance, travel to the directory which holds the server using: "cd project". Then use the following command to run the server: "node server.js". Now using a seperate powershell window, type in the following command to connect to the instance:
"ssh -L 9999:localhost:3000 student@134.117.132.194". 
Now you can go to your web browser and access the server using the following url: "localhost:3000"

How To Test:
To start with, open one brower normally and open another one in incognito, then go to the "localhost:3000" url on both. In order to test this, travel to the login hyperlink at the top left of the page. You can click on the others but the only two that will work properly is login and homepage, until you have successfully logged in/registered a new user. You can connect using the following accounts {username: james, password: password}, {username: user1, password: user1} or {username: rick, password: jones}. You can also register a new account if you wish but the username has to be unique. If you attempt to access pages without proper authorization, you will be served a status error page. Once you have successsfully logged in/registered, you will be taken to your own user profile with all your basic profile information. You will be able to edit or change profile details and other things but only if you have the proper contributing user permissions. Next, you can use the hyperlinks at the top to navigate between any of the 3 search engines. The searching for persons is not probably implemented, just as a warning. The best of the three search engines is the movie search function, you will be able to travel to individual movie pages through hyperlinks as well as navigate your way to other pages without having to type! Just click on the available hyperlinks. Lastly, is user input functionality which will be available through the user-input page (the link is at the top left). 

To Restart back to the default state:
while its running, hold down your ctrl button and press c to stop it. Then rerun the server again using node server.js.