OpenShift Python project for Cloud Computing Exercise #4

# Introduction

This is a hello world Python project that deploys on RedHat's
OpenShift Developer Preview.

# Steps

1. Register with OpenShift using Github credentials at https://api.preview.openshift.com/

2. Open the OpenShift console: https://console.preview.openshift.com/console/

3. Create a new Project

4. We're going to add a Python component to your project.  First, you
   need a Github repo.  You're welcome to fork this repo if you like.
   The important files are:

	  * [app.py](app.py) - must start a service that listens on port 8080 forever
	  * [requirements.txt](requirements.txt) - list of Python dependencies
	  
   NOTE: this worked for me, but I suspect OpenShift should have a
   better boiler-plate repo somewhere.  Let me know if you find it!
	  
5. Back to the OpenShift console, Add new Python2.7 component with
   your github repo's url
	  
6. Add OpenShift's webhook url to your github repo
   
7. Back to the OpenShift console, wait for your project to rebuild,
   then click the link in the upper right corner of the screen.  That
   should be your application printing "Hello World".  Congratulations!
   
8. Clone your repo locally, change app.py and push the changes.
   OpenShift will automatically rebuild it using the webhook you added
   earlier.

There's a command-line interface too, at
https://console.preview.openshift.com/console/command-line.  You can
get a token to log in at
https://api.preview.openshift.com/oauth/token/request

   
Cheers!

Noel Burton-Krahn <nburtonk@cisco.com>
