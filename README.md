# challenge6
Tech challenge for ENTO - Problem 1
## Initial local workstation setup
1. You need GIT, a web browser and a SSH client
2. Run `git clone https://github.com/TME520/challenge6.git`
3. Ask IT for your AWS Web Console credentials
4. Also ask IT for your EC2 SSH keypair (name format: *yourname-ec2key*)
## Starting a server
1. `git pull` your local code repository in order to make sure you have the latest version of the code,
2. Log into [AWS Web Console](https://console.aws.amazon.com). Use the credentials provided by IT on induction day,
3. Click on *CloudFormation*
4. Click on *Create Stack*
5. Click *Upload a template file*, then point to the CF template
6. Click *Next*,
7. Name your stack the way you want. Stack name can include letters (A-Z and a-z), numbers (0-9), and dashes (-),
8. In *KeyName*, select the keypair created for you by IT,
9. Click *Next*,
10. Click *Create stack*,
11. Click on the *Events* tab and wait for your stack to be created,
12. Click on the *Outputs* tab, it contains informations on how to SSH into your webserver,
13. Run this to see if instance creation went well after you SSH into it: `sudo less /var/log/cloud-init-output.log`,
14. You can run `python3 /home/ec2-user/hello.py` to check if Python3 is working.
