# Google Cloud Fundamentals: Getting Started with Cloud Marketplace 

## Overview
In this lab, you use Cloud Marketplace to quickly and easily deploy a LAMP stack on a Compute Engine instance. The Bitnami LAMP Stack provides a complete web development environment for Linux that can be launched in one click.

## Component 	                 Role
   -Linux 	                 -Operating system
   -Apache HTTP Server 	     -Web server
   -MySQL 	                 -Relational database
   -PHP 	                 -Web application framework
   -phpMyAdmin 	             -PHP administration tool
   
## Objectives
In this lab, you learn how to launch a solution using Cloud Marketplace.

## Task 1: Sign in to the Google Cloud Platform (GCP) Console
For each lab, you get a new GCP project and set of resources for a fixed time at no cost.

    -Make sure you signed into Qwiklabs using an incognito window and endavour to finish the lab with the time allocated to you.
    -When ready, click img/start_lab.png.
    -Note your lab credentials. You will use them to sign in to Cloud Platform Console. img/open_google_console.png
    -Click Open Google Console.
    -Accept the terms and skip the recovery resource page.
    -Do not click End Lab unless you are finished with the lab or want to restart it. This clears your work and removes the project.
    
## Task 2: Use Cloud Marketplace to deploy a LAMP stack
    -In the GCP Console, on the Navigation menu (Navigation menu), click Marketplace.
    -In the search bar, type LAMP
    -In the search results, click LAMP Certified by Bitnami.
    -If you choose another LAMP stack, such as the Google Click to Deploy offering, the lab instructions will not work as expected.
    -On the LAMP page, click Launch.
    -If this is your first time using Compute Engine, the Compute Engine API must be initialized before you can continue.
    -For Zone, select the deployment zone that Qwiklabs assigned to you.
    -Leave the remaining settings as their defaults.
    -If you are prompted to accept the GCP Marketplace Terms of Service, do so.
    -Click Deploy.
    -If a Welcome to Deployment Manager message appears, click Close to dismiss it.
    -The status of the deployment appears in the console window: lampstack-1 is being deployed. When the deployment of the infrastructure is 
     complete, the status changes to lampstack-1 has been deployed.
    -After the software is installed, a summary of the details for the instance, including the site address, is displayed.

Note: After following he steps above, Click Check my progress to verify the objective. If the circle turns Green then you followed all the instructions. If it turns red it means that you missed other steps. Please go back and follow all the steps.

## Task 3: Verify your deployment

    -When the deployment is complete, click the Site address link in the right pane.

    -Alternatively, you can click Visit the site in the Get started with LAMP Certified by Bitnami section of the page. A new browser tab
     displays a congratulations message. This page confirms that, as part of the LAMP stack, the Apache HTTP Server is running.
    -Close the congratulations browser tab.
    -On the GCP Console, under Get started with LAMP Certified by Bitnami, click SSH.
            In a new window, a secure login shell session on your virtual machine appears.
    -In the just-created SSH window, to change the current working directory to /opt/bitnami, execute the following command below:
            cd /opt/bitnami
    -To copy the phpinfo.php script from the installation directory to a publicly accessible location under the web server document root, 
     execute the following command below:
            sudo sh -c 'echo "<?php phpinfo(); ?>" > apache2/htdocs/phpinfo.php'

               The phpinfo.php script displays your PHP configuration. It is often used to verify a new PHP installation.
    -To close the SSH window, execute the following command:
    -exit
    -Open a new browser tab.
    -Type the following URL below, and replace SITE_ADDRESS with the URL in the Site address field in the right pane of the lampstack page.
            http://SITE_ADDRESS/phpinfo.php
                 A summary of the PHP configuration of your server is displayed.
    -Close the phpinfo tab.

## Congratulations!
         In this lab, you deployed a LAMP stack to a Compute Engine instance.
                 End your lab

