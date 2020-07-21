# Full Stack with PICK Tutorial
In this *Full Stack with PICK Tutorial* we show you how to integrate multiple technologies to span the stack. Including docker, jBASE, REST and Vue.js.  
  
## License
[MIT](https://opensource.org/licenses/MIT)  
  
Copyright (c) 2020-present, Zumasys

You can use the video or this document to get a docker container of Jbase running on your system and get the demo data installed on it.  Future videos will walk you through the rest of the process to create a website that will pull data in and out of your multivalue database.

Do not worry if you are unfimiliar with dockers the process is very simple and this will walk you through each step. 

The first step you will need to do is go to Docker.com and register for a free account.  To register you click on the get started button at the top right. Scroll down to choose a plan. Then click on the Signup for Free. After you register you will get an email that you will use to verify your account.

Now to download and install the docker application again you click on the get started button.  Scroll down to the docker desktop on left and download the version for you OS. Run the install once the download is completed. After the install is complated you will need to reboot your computer.

Once you have the docker application installed you will need to download the jbase docker. You do this by opening a command prompt window and from the command prompt window type: 
docker pull zumasys/jbase_base

This will download the latest jBase Docker container with jBase already set up.

Next we will start the docker by typing in the following command from your command window
	docker run -it -p 20002:20002 zumasys/jbase_base
 
Now that you are in your jbase docker you can create a account in jbase that will store the the demo file. Simply execute the command CREATE-ACCOUNT DEMO  

To logto the demo account type in LOGTO DEMO

We will now create a basic program file to hold the program that will create the demo file.  The command is CREATE-FILE BP TYPE=UD  The type of UD will create a directory type file which is the prefered type for basic programs in jBase.

To load the source code down the program file from the github open a browser and go to this site:  https://github.com/pickmultivalue/full-stack-with-pick-tutorial  

Next you will on the on the back-end folder in about the middle of the page. 
Then click on setting-up-Jbase-demo-data folder.

We will simple cut and paste the program file into Jbase. So please click on the program name an then highlight the program and copy it.

Now go back to your jbase docket and to tdit the program type in JED BP MAKE.DEMO. Paste the program in from the above step. 

In jBase to create an executable program you need to compile and catalog the program. To File the program, compile and catalog in one step by hitting the escape key and typing FIBC

Now we are ready to create the demo file by running the program with the command RUN BP MAKE.DEMO.  The program will ask two questions first the number of records you want to create and the second is file name please use DEMO.FILE for the filename as that is what will be used in future videos.  The program randomly generates the data for the a static list of each data element

Lastly we list the file to see that the file was created and populated the command is LIST DEMO.FILE FIRSTNAME LASTNAME ADDR1

Now that you have jBase up and running and have your demo account and demo data please watch the next video in the series.
