## How to Create Ec2 Template ?

Step-1 log in your aws console and click on services and scroll down and search for Ec2 template>Create launch template
Step-2 - Enter the template name -



![Image](https://github.com/user-attachments/assets/d5efed1a-e070-41d0-9490-a0f490bf258a)


>  Browse and  select the image what type of image you want . since i want ubuntu so i have selected the ubuntu  like -


![Image](https://github.com/user-attachments/assets/66e0c9a0-5266-453d-8f8e-859181a3af0c)

Step-3- Select Instance type what ever as per requirement -



![Image](https://github.com/user-attachments/assets/904e3628-d2e9-4fc8-be1a-8022bc959297)

and select keypair or create a new keypair-



![Image](https://github.com/user-attachments/assets/18ee2efb-70ff-4448-afe5-b16351929981)

In network you can use you exiting security group or you can create one new as per requirement.



![Image](https://github.com/user-attachments/assets/a8e0aad8-3c42-4a86-8bf9-14216856a62a)

Step- 4- Enter the user data -


![Image](https://github.com/user-attachments/assets/26095475-11fa-4a3d-bd26-9f0a66879e83)


```
#!/bin/bash
sudo apt-get update 
sudo apt-get install nginx -y
sudo systemctl start nginx

sudo systemctl status nginx
```


