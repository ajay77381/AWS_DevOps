### How to install & configure the AWS CLI  in Ubuntu ?

To configure AWS credentials and set up to work with AWS, you'll need to follow these steps:

Install AWS CLI (Command Line Interface):
Make sure you have the AWS CLI installed on your machine. You can download and install it from the [AWS CLI download page](https://aws.amazon.com/cli/).

The following aws configure command example demonstrates user input, replaceable text, and output:

Enter **aws configure**  at the command line, and then press Enter.

The AWS CLI outputs lines of text, prompting you to enter additional information.

Enter each of your access keys in turn, and then press Enter.

Then, enter an AWS Region name in the format shown, press Enter, and then press Enter a final time to skip the output format setting.

The final Enter command is shown as replaceable text because there is no user input for that line.

 `
sudo apt install awscli
`

> $ aws configure

AWS Access Key ID [None]: AKIAIOSFODNN7EXAMPLE

AWS Secret Access Key [None]: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY

Default region name [None]: us-west-2

Default output format [None]: ENTER
