


# What is What is Node.js?

Node.js is an open-source JavaScript runtime environment programming platform. Node.js can run on Windows, Linux, Unix, macOS, and more. It allows developers to create back-end functionality using JavaScript. Being able to install Node.js on Ubuntu or another OS is a boon for JavaScript users worldwide. If you're into JavaScript like me, installing Node.js on Ubuntu or any other operating system is a great idea. It's like having one language for all your development tasks. 

 

![Image](https://github.com/user-attachments/assets/bb80fc19-e6a4-4f2d-82c1-2f8460b958b5)

Essentially, what Node.js does is take the functionalities and features of the JavaScript language and package them into modules. It takes JavaScript, originally designed to run in a browser, and upgrades it to run in other environments. It's a versatile tool that expands the possibilities of what you can achieve with JavaScript beyond the traditional browser setting.

Because these upgrades are packaged into Node.js developers can now use JavaScript for frontend and backend development making JavaScript a full-stack language. 

In the past, Node.js was only designed to serve real-time performance and push-back architectures. Since then, Node.js has developed into a crucial component of server-side scripting for event-driven, non-blocking servers. Today, Node.js powers most traditional websites and API services. Node.js uses an event-driven, non-blocking I/O architecture and the V8 JavaScript runtime engine as its primary power source. 

## Prerequisites to Install Node.js on Ubuntu

Before installing the updated node version on Ubuntu, you must ensure that you’ve accumulated all the necessary knowledge. Also, make sure you’ve downloaded all required installation files and elements. 

- It would help a lot if you had a basic understanding of JavaScript and its syntax. This enables you to pick up Node.js easily. 
- You may work on server-side coding by having a basic grasp of an object-oriented programming (OOP) language. 

## Hardware Requirements 
Below are the hardware requirements for installing Node.js on Ubuntu. 

- Node.js does not need a complex hardware configuration to work; most machines nowadays are compatible.
- Node.js install on Ubuntu requires a stable hard drive for it to work. 
- You should have the necessary prerequisites to install Node.js for Ubuntu.
- Virtually all modem computers can run Node.Js, including miniature computers like BeagleBone or Arduino YÚN. 
- The Random-Access Memory (RAM) of your system should be up to 4GB and your system storage should be at least 256GB of Hard Disk Space. 

## How to Install Node.js on Ubuntu? [Step-by-Step]


Let me take you through the three methods below to install Node.js on your Ubuntu machine.

1- Installing the Stable Version for Ubuntu 
2- Install Node.js Using a PPA 
3- Install Node.js Using Node Version Manager (NVM)

# Note- Here i am following the method 3 .If you want to install with other methode then follow the berlow URL-

Reference- https://www.knowledgehut.com/blog/web-development/install-nodejs-on-ubuntu#how-to-uninstall%C2%A0node.js%C2%A0from-ubuntu?%C2%A0


# Method 3: Install Node.js Using Node Version Manager (NVM):

The NVM (Node Version Manager) is also used to install Node.js. It has the advantage of displaying a list of all available Node.js versions, from which you can choose to either install the most recent version or a specific version. Use the instruction below to install Node.js ubuntu command line. 

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

Now install the latest Node.js on NVM using the command below. 

```
nvm install node 
```


![Image](https://github.com/user-attachments/assets/2231d6ac-31d7-4c49-b079-f68536fdeeb9)



With the above, you will install node and npm on Ubuntu. 

# How to Verify if Node.js is Installed on Ubuntu?
Now you’ve installed Node.js, you can verify the installation to check if the installation was successful. To confirm the installation, you must run the following Linux commands on your terminal. 

To check the Node.js version type: 

```
node -version  
```

And to check the npm version, type: 
```
npm --version 
```

The Node.js and npm version names should be displayed on the terminal if they were successfully installed. 

# Create Demo Web Server: 

Step 1: Open a code editor and select a working directory. 

Step 2: Create a new file called index.js in the root of the working directory. 

Step 3: Copy and paste the codes below inside the index.js file. 


````
// Importing the http module 
const http = require("http") 

// Creating server 
const server = http.createServer((req, res) => { 
	// Sending the response 
	res.write("This is the response from the server") 
	res.end(); 
}) 

// Server listening to port 3000 
server.listen((3000), () => { 
	console.log("Server is Running"); 
})

````
Step 4: Run index.js file using below command:l.
``
node index.js
``

![Image](https://github.com/user-attachments/assets/a280f881-9317-4cf6-9c48-3eb29a53e840)

# Output: Now open your browser and go to http://localhost:3000/, you will see the following output:



![Image](https://github.com/user-attachments/assets/064e29b6-c716-4e82-9409-2e54f43e094e)


# What difficulty i faced in to making the NodeJS build.

1- once we exit form shell what is happening website stopped and we are not able to see in webpage.

**Solution**- we have just add the & in command so  it can run in background. Like below command-

```
node index.js &
```



2- Once we restarted the system what i found i am not able to find where i have installed the nodeJs  in WSL while i have already installed and tested before restart.

Solution- We found we have installed the multiple version of Ubuntu in system so we first unregistered and uninstalled the all version of ubuntu and kept only what i required. Like i required Ubuntu22.40.6 and set it default in wsl.


Note- We have done the nodeJs build on local as well as on GCP cloud in gcloud shell.


# Uninstalling a distro via the settings or store didn't work for me. What did was:

1- Enter a cmd or PowerShell prompt,
2- wsl -l to see a list of installed distro names
3- wsl --unregister <DistroName>

I had to execute wsl --setdefault Ubuntu-22.04 afterwards (otherwise, docker-desktop would have been the default WSL distribution)




