https://www.youtube.com/watch?v=wGl7V2HvSZ0&list=PLVAvGzDq49UlSP8G-2HgC4-kKehVSysCb&index=1


# What is Bigfix ?
Bigfix is a system management software product for managing large group of computersystem. Big fix use for patch mangement ,Power mangement software distrubutin , Operating system deployment and to mange Hardware and software inventory.

## Bigfix Architecture _Terms

![image](https://github.com/user-attachments/assets/c9e87958-8ece-4db6-9161-41f59ea4c3e0)


## Introduction to Bigfix - Basic Architecture

![image](https://github.com/user-attachments/assets/2de84857-28bf-4bf6-a2e0-0c0c2cbc1ebe)


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







