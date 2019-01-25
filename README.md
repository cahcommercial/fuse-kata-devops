  # FUSE DEVOPS AUTOMATION ENGINEERING KATA

* All kata requirements do not need to be coded in order for the kata to be submitted, however requirements implemented 
  should be done so using best practices.
* This is a showcase of skill,not speed.
* When submitting, please let us know what kata requirements were implemented.
* Spend no more than two hours on tha kata.

## Available Kata's
* [Linux Cloud Automation Engineer](https://github.com/cahcommercial/fuse-kata-devops/blob/master/README.md#linux-cloud-automation-engineer) 
* [Windows Cloud Automation Engineer](https://github.com/cahcommercial/fuse-kata-devops/blob/master/README.md#windows-cloud-automation-engineer)

## Linux Cloud Automation Engineer

* The technical exercise for a Fuse Linux DevOps Automation Engineer covers three technologies / concepts that are prevalent in the Fuse environment. In this exercise you will need to create a server in the AWS public cloud (preferably in your personal account), write a simple Chef cookbook, and write a simple Dockerfile. For Chef you will need to write a cookbook that installs an Apache web server listening on port 80, and for Docker you will need to build a containerized NGINX that listens on port 8080 and redirects to port 80 (the Apache web server). The Chef and Docker artifacts need to be deployed to the AWS instance you create, and Fuse will need SSH access to that instance to review the artifacts.
  
    ## Kata Instructions
  
     ## Amazon Web Services (AWS)
     * In this section you need to create an Ubuntu AWS EC2 instance where the following sections' artifacts will be deployed to:
        * Build an amazon node (t2.micro is sufficient) using Ubuntu 14.04 with a public IP address 
        * Secure it (aside from your local ip or jump box)- expose ports 22, 80, and 8080 to the following IP: 52.7.76.128
        * Create a local account which has the ability to login via SSH and sudo to root.  This account will be used to verify the configurations of the host.

    ## Chef
    * In this section you will write and deploy a simple Chef cookbook that installs and configures Apache.
     * Write a Chef cookbook that performs the following tasks:
        * Install Apache HTTP Server
        * Create a default HTML page named fuse.html that displays
          * Hostname of your instance
          * IP of your instance
          * A link to the location containing the log output for the chef client execution. (Make sure the log can be downloaded.)
        * Configure Apache to load fuse.html as the default page
        * Manually install the ChefDK on the server created in the AWS Web Services section
        * Run the Chef cookbook with chef-solo on the server
        * Write the results of the chef run to a log file, as this is needed for the link in fuse.html

    ## Docker
     * In this section you will write and deploy a Dockerfile
       * Create a Dockerfile that meets the following requirements:
         * Ubuntu 14.04 base image
         * Installs NGINX
         * Configures NGINX to redirect the browser from port 8080 to port 80
         * Exposes port 8080 for the container
         * Build and run the docker container in detached mode, exposing port 8080 on the EC2 instance

    ## End result
     * Only the IP listed above should be able to access ports 22, 80 and 8080.  No other ports should be open to the internet.
     * Accessing the server on port 8080 should redirect to port 80 and display the information from fuse.html
 
 
 
## Windows Cloud Automation Engineer

    ## Kata Instructions
    
* Write 3 Microsoft Powershell scripts which will satisfy the following requirements:

  *	Use DSC and powershell to push configuration mofs that will:
    *	Execute a powershell script that runs Tues, Thursday and Saturday at 8AM
    * Ensure the following exists in the registry, “HKLM\System\DSCTest”, with a dword named “BuildNumber” that contains the value of 1

  *	Use powershell and AWS to backup files:
    *	Copy all databasebackupXX.bak files from any folders under E:\Backups to D:\MovetoS3. When doing so, organize the D:\MovetoS3 how you see fit
    *	Move any backup files older than 90 days  to an S3 bucket named S3-backups-123. Again, organize how you see fit.

  *	Create a powershell script to install 3 different apps, (app1.msi, app2.exe, app3.msi) without user interaction, and ensure the process is logged to C:\Temp\TriApp-Install.log:
    *	The apps must be installed in order, as they are dependent on the earlier installs.
    * If any app fails to install, stop the installation and report the error in the log.


