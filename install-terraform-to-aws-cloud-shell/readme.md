AWS cloud shell is a linux based terminal, OS often reffered as "Amazon Linux". 

login into aws management console as root or an IAM user with admin privellages

open aws cloud shell and wait for it to load

if you do "terramform -help" you will get a cmdlet not found error. This indicates that cloud shell terminal does not know what terraform is. We will need to install.

Run the following below commands in order.

Install yum-config-manager to manage your repositories:
sudo yum install -y yum-utils


Use yum-config-manager to add the official HashiCorp Linux repository:
 sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/AmazonLinux/hashicorp.repo


Install Terraform from the new repository.
sudo yum -y install terraform


Now you can verify the install by running 
terraform -help

If you get feedback with list of help commands terraform is now installed.

Next you want to install the plugin that will terraform and aws to interact. Run below.
terraform -init

This completes onboarding terraform into AWS cloud shell. 

