https://www.youtube.com/watch?v=wGl7V2HvSZ0&list=PLVAvGzDq49UlSP8G-2HgC4-kKehVSysCb&index=1


Use full Link-
https://forum.bigfix.com/c/events


# What is Bigfix ?
Bigfix is a system management software product for managing large group of computersystem. Big fix use for patch mangement ,Power mangement software distrubutin , Operating system deployment and to mange Hardware and software inventory.

## Bigfix Architecture _Terms

![image](https://github.com/user-attachments/assets/c9e87958-8ece-4db6-9161-41f59ea4c3e0)


## Introduction to Bigfix - Basic Architecture

![image](https://github.com/user-attachments/assets/2de84857-28bf-4bf6-a2e0-0c0c2cbc1ebe)

# What is Fixlet in HCL Hot Fix ?

In HCL BigFix, a fixlet site is a collection of fixlets, tasks, and analyses related to a specific BigFix application. Fixlets and tasks are central to BigFix and are used by BigFix Inventory to perform actions on selected computers

- Port 21/80/443 is use to collect Fixlet messages over the internet from the content provider such as RedHat.
- Dedicated port is used for http communication between server relay and clients
- Dedicated port is user for https cmmunications between servers and consoles.
- Relays and the BES server use TCP to alert other relays about  updates.
- Relays use a UDP to aleart the client abouts updates.
- Relays are use to shae the server load
- Typically a relay is deployed for every 500-5000 computers
- Client are typically PCs or workstations but can include any device that can benifit from patches and updates

## Installing the big fix

![image](https://github.com/user-attachments/assets/bc958e46-3d07-4414-8c64-3bee4cc64a14)

![image](https://github.com/user-attachments/assets/84dd632c-32f2-4413-996c-9f9f373dec2c)

![image](https://github.com/user-attachments/assets/2f69b42a-d8c7-4115-a4e4-edf94ceff8eb)


![image](https://github.com/user-attachments/assets/44f7170b-195f-42a1-9bad-ca1cd9148769)

![image](https://github.com/user-attachments/assets/b4e7b4a8-86a8-4e75-8695-4596e0486656)

![image](https://github.com/user-attachments/assets/5f511458-0136-4d45-b3b3-f1d1221e8eb6)

![image](https://github.com/user-attachments/assets/7120817e-8205-499e-8ef3-02599946a824)

![image](https://github.com/user-attachments/assets/6e9c28f2-0a3f-434f-907f-21a2e8675cca)

![image](https://github.com/user-attachments/assets/ecfc96f1-d8fa-42dc-bc8d-1c0df8e07c2c)

![image](https://github.com/user-attachments/assets/ec93b6fb-6150-4da4-a2fe-fbccfc189862)




Reference URL- https://help.hcl-software.com/bigfix/9.2/platform/Platform/Adm/c_getting_authorized.html

## Before Installing

Configuring a Local Firewall
If you have defined an active firewall on the computer where you are installing the BigFix server, you can decide to configure this firewall during the BigFix server installation in one of the following ways:

During an interactive installation, the installation programs detects if a local firewall is active and you can specify if you want to configure it for the BigFix server.
During a silent installation, you can set CONF_FIREWALL=YES in the response file to require the firewall configuration. For more information, see Silent installation.
When you specify to configure the firewall, the following two ports are opened:
Port 52311 for UDP and TCP/IP
Port 80 for Web Reports and TCP/IP

## Modifying port numbers
By default, the server uses port 52311 to communicate with the clients, but you can choose any port number (although you should avoid the reserved ports between 1 to 1024 because of potential conflicts and difficulty managing network traffic).

Your choice of the server port number is factored into the generation of the masthead, which specifies URLs for the action, registration, reporting, and mirror servers. As a consequence, you must finalize your port number before installation.

Consoles use port 52311 to connect to the server.

# Installing on Windows systems

Now that you understand the terms and the administrative roles, you are ready to get authorized and install the programs.

Because BigFix is powerful, you might want to limit access to trusted, authorized personnel only. The product depends on a central repository of Fixlet actions called the Action site, which uses public/private key encryption to protect against spoofing and other unauthorized usage. To get started, you need authorization from IBM by getting a License Authorization file, which will have a name like CompanyName.BESLicenseAuthorization.

The Installer program collects further information about your deployment and then creates a file called the action site masthead. This file establishes a chain of authority from the BigFix root all the way down to the Console operators in your organization. The masthead combines configuration information (IP addresses, ports, and so on) and license information (how many Clients are authorized and for how long) together with a public key that is used to verify the digital signatures. To create and maintain the digital signature keys and masthead, you use the BigFix Installer, which you can download from IBM.

Installation Steps
To install the product, perform the following steps:

1- Download BigFix.
2- Request a license and create the masthead using the installer program. When it prompts you for the authorization file, use the License Authorization file (*.BESLicenseAuthorization) that you created using your License Key Center account or, in the case of a Proof-of-Concept evaluation, that was provided to you by your IBM Technical Sales Representative.
3-  Run the BigFix installation.

## Step 1 - Downloading IBM BigFix
Download BigFix from the IBM Passport Advantage portal.

You can download BigFix also from the support site at http://support.bigfix.com/bes/install/downloadbes.html or from the DeveloperWorks trial site at http://www.ibm.com/developerworks/downloads/tiv/endpoint/. The demonstration trial installer is the same installer program as that used for a normal production installation.

To install the server component download the following e-images from Passport Advantage:

Table 1. Software required for installing BigFix Server
Software Name	Part Number	Image
IBM BigFix Platform Install V9.2.6 for Multiplatforms	CN7CZML	BigFix_Pltfrm_Install_V92.zip
To extract the BigFix Windows server installation files, perform the following steps:

Copy the BigFix Server zip file BigFix_Pltfrm_Install_V92.zip to your Windows Server.
Expand the zip file using the following command:
unzip "BigFix_Pltfrm_Install_V92.zip"
You can find the setup.exe file to install the Windows Server in the BigFix_Pltfrm_Install_V92 folder.

## Step 2 - Requesting a license certificate and creating the masthead

Before you perform the steps below, you must have purchased a license and obtained a BigFix license authorization file (*.BESLicenseAuthorization) using your License Key Center account or, in the case of a Proof-of-Concept evaluation, that was provided to you by your IBM Technical Sales Representative.

When you have your license authorization file, you are ready to request a license certificate and then create a personalized site masthead that, in turn, allows you to install and use BigFix. The masthead includes URLs for the Server CGI programs and other site information in a signed MIME file. The masthead is central to accessing and authenticating your action site. To create the masthead and activate your site, follow these steps:

1- Run the BigFix installer BigFix-BES-9.2.6.xxxx.exe, where 9.2.6.xxxx is the version of the installer). When prompted, choose Production installation and accept the Software License Agreement. On the welcome screen, click Next.

# Note: If you choose the Evaluation installation, consider that this type of installation does not support the enhanced security option. For more information about this feature, see Security Configuration Scenarios.

2- After reading and accepting the License Agreement, select I want to install with an IBM Endpoint Manager license authorization file, to create your Private Key and Masthead

![image](https://github.com/user-attachments/assets/31b7ed17-c128-4dd4-b70d-936f5a22016d)

3- Enter the location of your license authorization file, which has a name like CompanyName.BESLicenseAuthorization
![image](https://github.com/user-attachments/assets/6462662a-a9d2-4d71-b98e-188b9b14688b)

4- Specify a DNS name or IP address for your BigFix server and click Next. The name that you enter in this field is recorded in the license and used by clients to identify the BigFix server.
Note: Enter a DNS name, such as bes.companyname.com, because of its flexibility when changing server computers and doing advanced network configurations. This name is recorded into your license certificate and is used by clients to identify the BigFix server. After your license certificate is created, the DNS name cannot be changed. To change the DNS name, you must request a new license certificate, which requires a completely new installation.

5- Type a site credential password to allow you to create a site admin key for your deployment. Type your password twice (for verification), and specify a key size (from 2K to 4K bits) for encrypting the private key file. Click Create.

![image](https://github.com/user-attachments/assets/0fa07688-52f5-4502-bf8a-4d8d097142e9)

In this way you generate a private/public key pair used to create and authorize all the BigFix users.

6- Save your private key (license.pvk) file from the Browse for Folder dialog in a folder with secure permissions or on a removable drive, such as a PGPDisk or a USB drive. Click OK.

Important: If you lose the private key file, a new license certificate needs to be created, which requires a completely new installation. In addition, anyone with the private key file and password have full control over all computers with the BigFix clients installed so ensure that you keep the private key file and password secured.

7- You are requested to send the request file to IBM for license verification. If you have internet connectivity, choose the option to submit your request over the internet. In this case, a request file is sent to IBM for license verification. This request consists of your original authorization file, your server DNS name and your public key, all packaged into a single file.

![image](https://github.com/user-attachments/assets/a835ff96-dd94-4aca-8935-3df60280d71d)

8- If you select to submit the request over the Internet and your enterprise uses a proxy to access the Internet, click Set Proxy. The Proxy Settings panel opens. In this panel you can configure the proxy connection.

![image](https://github.com/user-attachments/assets/8753dc52-48ff-4e8b-bd48-16ba4394130b)

9- Specify:
The hostname or IP Address and, optionally, the port number to communicate with the proxy machine.
The credentials of the user defined on the proxy machine that must be used when establishing the connection.
The comma-separated list of hostnames, subdomains, IP addresses that identify systems in the BigFix topology that must not be reached thru the proxy. By default, BigFix V9.2 prevents diverting internal communications towards the proxy. If you set a value in this field, you overwrite the default behavior. To ensure that internal communications are not directed to the proxy, add localhost, 127.0.0.1, yourdomain.com, IP_Address to the list of exceptions specified in this field.
Whether or not the proxy is enforced to attempt tunneling. By default the proxy does not attempt tunneling.
The authentication method to use when establishing the communication. You can either let the proxy choose the authentication method or you can impose to use specific authentication methods.
Note: If you want to enable FIPS mode, select an authentication method other than digest.
You can click Test Connection to verify if the connection with the proxy that you configured can be successfully established. For more information about the values and the syntax to use in these input fields, see Setting a proxy connection on the server.
Click OK save the settings and return to the Request License panel.

10- Click Request. The Wizard retrieves your license certificate (license.crt) from the BigFix License server.
Alternatively, if you are on an airgap without internet connectivity, choose the option to save the request as a file named request.BESLicenseRequest. Copy the file to a machine with internet connectivity and submit your request to the URL of the BigFix website shown in the installer. The page provides you with a license.crt file. Copy the file back to the installation computer and import it into the installer.

11- From the Request License dialog, click Create to create the masthead file

![image](https://github.com/user-attachments/assets/a9c58623-f1cd-408f-b1e5-c5895c08c1c6)

12- Enter the parameters of the masthead file that contains configuration and license information together with a public key that is used to verify digital signatures. This file is saved in your credential folder.

![image](https://github.com/user-attachments/assets/fa86442f-b084-4b68-9ccc-9a50b99144f5)

You can set the following options:
Server Port Number:

In general, you do not need to change this number. 52311 is the recommended port number, but you can choose a different port if that is more convenient for your particular network. Typically, you choose a port from the IANA range of private ports (49152 through 65535). You can use a reserved port number (ports 1-1024), but this might reduce the ability to monitor or restrict traffic correctly and it prevents you from using port numbers for specific applications. If you do decide to change this number after deploying the clients, BigFix will not work correctly. For additional information, see Modifying port numbers.
Note: Do not use port number 52314 for the network communication between the BigFix components because it is reserved for proxy agents.
Gathering Interval:
This option determines how long the clients wait without hearing from the server before they check whether new content is available. In general, whenever the server gathers new content, it attempts to notify the clients that the new content is available through a UDP connection, circumventing this delay. However, in situations where UDP is blocked by firewalls or where network address translation (NAT) remaps the IP address of the client from the servers perspective, a smaller interval becomes necessary to get a timely response from the clients. Higher gathering rates only slightly affect the performance of the server, because only the differences are gathered; a client does not gather information that it already has.
Initial Action Lock:
You can specify the initial lock state of all clients, if you want to lock a client automatically after installation. Locked clients report which Fixlet messages are relevant for them, but do not apply any actions. The default is to leave them unlocked and to lock specific clients later on. However, you might want to start with the clients locked and then unlock them on an individual basis to give you more control over newly-installed clients. Alternatively, you can set clients to be locked for a certain period of time (in minutes).
Exempt the following site URL from action locking:
In rare cases, you might need to exempt a specific URL from any locking actions. Check this box and enter the exempt URL.
Note: You can specify only one site URL and it must begin with http://.
Require use of FIPS 140-2 compliant cryptography
Check this box to be compliant with the Federal Information Processing Standard in your network. This changes the masthead so that every BigFix component attempts to go into FIPS mode. By default, the client continues in non-FIPS mode if it fails to correctly enter FIPS, which might be a problem with certain legacy operating systems. Be aware that checking this box can add a few seconds to the client startup time.
For more information see FIPS 140-2 cryptography in the BigFix environment.

Note: Enabling FIPS mode might prevent the use of some authentication methods when connecting to a proxy. If you selected to use a proxy to access the Internet or to communicate with BigFix subcomponents, ensure that the proxy configuration is set up to use an authentication method other than digest.
Allow use of Unicode filenames in archives:
This setting specifies the codepage used to write filenames in the BigFix archives. Check this box to write filenames UTF-8 codepage.
Do not check this box to write filenames using the local deployment codepage, for example Windows-1252 or Shift JIS. If you run a fresh install of BigFix V9.2, by default, the filenames are written in UTF-8.
Note: If you upgraded your BigFix environment to V9.2, by default, the filenames are written in the local deployment codepage.
Click OK when you are finished.

13- Choose the folder in which to install the BigFix component installers. The BigFix Installation Guide wizard is launched to lead you through the installation of the BigFix components.
Note: This step creates the installers for the BigFix client, BigFix console, and BigFix server, but does not install the components.
Note: The private key (license.pvk) authorizes the creation and rotation of server signing keys, which are trusted by all agents. This key is not sent to IBM during the license certificate creation process, and must be carefully protected. To reinstall the server on your workstation, you must reuse the stored BigFix credentials. If you did not save them, when you reinstall the server you must regenerate them.












