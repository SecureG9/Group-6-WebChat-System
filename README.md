# README
## <b>Websocket Based Chat Application
### <b>Project Description:</b>

The goal of this project was to design, developand secure a multi-party chat application that adheres to a collaboratively standardized protocol among peers. This application can facilitate secure communication between multiple parties, incorporating advanced secure coding practices and intentional vulnerabilities.

The secure chat application will provide the following features:
<ul><li>Listing all members of the chat system
<li>Private messaging between individual participants
<li>Group messaging to all participants
<li>Point-to-point file transfer
<ul>
### <b>List of Contents:</b>
<ol><li>Technologies Used</li>
  <li> Installing the code</li>
  <li> Prerequisites</li>
  <li> Configuration on the Server and Client</li>
  <li> Starting the Server</li>
  <li> Running the Client</li>
  <li> Usage</li>
  <li> Our Team</li>
</ol>
### <b>1) Technologies Used:</b>
List of the main programming languages, frameworks, libraries, and tools we used to build this project:
<ul>
  <li>JavaScript</li>
  <li>HTML</li>
  <li>Websockets JS library "ws"</li>
  <li>Cryptography JS library "crypto"</li>
  <li>Config JS library "config"</li>
  <li>A Latest Updated Web Browser</li>
</ul>
### <b>2) Installing the Code</b>
###### <em>Instructions are Identical for Windows and Linux</em>
<ul>
<li>Install and configure the project locally.
<br><br>
<li>Clone this repository: 

# git clone https://github.com/username/project.git
Navigate into the project directory: cd <b>path</b>
# cd "path_to_repo_local"
### <b>3) Prerequisites:</b>

###### <em>Instructions are Identical for Windows and Linux</em>

<li>Install <b>Node.js</b><br><br>
We Recommend installing using the Prebuilt Installer Version<br>

<em>url</em>: https://nodejs.org/en/download/package-manager

<li>In the project directory created above intitalize a node js repository:
# npm -init 
<li>Install the depedencies using:
# npm install ws crypto config fs
<li> This satisfies the following requirements:
# const WebSocket = require('ws');
# const crypto = require('crypto');
# const config = require('config');
in case of error try independent install for all libraries
### <b>4) Configuration:</b>
###### <em>Instructions are Identical for Windows and Linux</em>

##### <b>a) Server Side:</b><br>

In the <b>"default.json"</b> file:
&nbsp;The IP and Server Domain name can be configured here:

<li><b>serverMapping</b> is the dictionary that maps domain names to ip addresses in the code. <br><br>
    Please include information of all servers you want to connect to<br><br>

# {
#     "serverMapping": {
#       "s1": "ws://IP_ADDRESS:5555",
#       "s2": "ws://IP_ADDRESS:5555"
#     }
<li><b>registeredUsers</b> is the dictionary that maps userid and hashed (sha256) password of all users connected on this server
#     "registeredUsers": {
#       "aryan@s1": "7549920a8f8c5dec3f1dcdb7a5eb7840ea1e52f2ee40fe70b6d1fb376aed3a8d",     #passwd123
#       "ash@s1": "7d082e414f09c5ca390197afe48109943e2597c782e58e4262b14303477c1b6b",       #passwd456
#       "shivang@s1": "12b0c9632941cc3aa7075eacc55d4919cadd5c1bd8690460e696bee538db87aa",   #passwd789
#       "buffer@s1": "buffer"
#     }
In the <b>"server.js"</b> file:
<li>Set server <b>Domain Name:
# const DOMAIN = "server_name";
##### <b>b) Client Side:</b>
In the Client code in the script section:<br><br>
Set the IP to the IP of the server you want to connect it to
# const ws = new WebSocket('ws://THE_SERVER_IP:5555');
### <b>5) Starting The Server:</b>
###### <em>Instructions are Identical for Windows and Linux</em>
##### Independently Running the server:
In the Terminal:
# PS C:\Users\Stewie\Desktop\server 01> node "c:\Users\Stewie\Desktop\server 01\server 01.js"
###### <b>OUTPUT:
# WebSocket server started on 5555:
##### Need to connect to other servers?
To connect to multiple servers, At the bottom of the server code in the main function:<br>
# async function main() {
#     const wss = new WebSocket.Server({ port: 5555 });
#     wss.on('connection', handler);
#     console.log("WebSocket server started on ws://192.168.225.66:5555");
#     await connectToServer("s2");
# }
You are able to add multiple statements to connect to multiple servers....YAY!!!!
# await connectToServer("DOMAIN_OF_TARGET_SERVER");
###### <b>OUTPUT:
# WebSocket server started on 5555
#Connected to server "DNAME" 
### <b>6) Running the Client:</b>
###### <em>Instructions are Identical for Windows and Linux</em>

Open the client code by opening it in any recently updated browser
### <b>7) Usage:</b>
###### <em>Instructions are Identical for Windows and Linux</em>
The GUI on the client side is quite intuitive and once a user logs in, they can:
<ul>
<li>send a target message to any user, 
<li>broadcast a message to all users, 
<li>file share with a specified target user. 
</ul>
The File shared is presented as a link in the message box as any message. The link can be clicked to download the file on the client machine

Please note: <b>the target user for the target message and file transfer are input in the same textfield. </b>
### <b>8) OUR TEAM </b>
<li>Aryan Puri
<li>Shivang Patel 
<li>Aashaykumar Shah
<li>Kartik Dangi

