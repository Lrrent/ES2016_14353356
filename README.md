# ES2016_14353356

***
###Overview
    This markdown file describes the steps of first project in Embedded Class. 
    There are steps for the installation of Ubuntu configuration.
    
###1.Installation of Ubuntu
    For installing Ubuntu system, you should first download Ubuntu iso(16.04 is the best choice for better compiling environment).   
    Then install this system in the virtual machine softwares(I choose VMWAREStation12).  
    
###2.Preparation of Installing
    Before we configure the environment, some softwares and plug-in should be installed first. 
    They can be installed by following orders:
    (1)sudo apt-get update
    (2)sudo apt-get install ant
    (3)sudo apt-get install openjdk-7-jdk(If fail downloading, choose openjdk-8-jdk alternatively)
    (4)sudo apt-get install unzip

###3.Package Unzipping
    After installing the Ubuntu system, we have to configure the compiling environment. 
    Here are significant steps before DOL configuration:
    (1)Unzip the DOL package in a new file
    (2)Unzip systemc package in a new file

###4.Package Compiling
    Move file pointer to the file of systemc and then enter following codes to configure the environment 
    ---> "../configure CXX=g++ --disable-async-updates"(quotation marks excluded). 
    If successful configuration, the information shown on the command line should be the same as texts below:
    ---Enable compiler optimizations : yes
    ---Include debugging symbols     : no
    ---Coroutine package for processes : QuickThreads
    ---Disable async_request_update  : yes
    ---Phase callbacks(experimental) : no
    ---Additional settings     :
    
###5.DOL Compiling
    Move to the DOL file and modify the path of systemc.inc and systemc.lib as where they are in your own computer      
    (specifically, for 64-bit system, "lib-linux" should be modified as "lib-linux64")
    The result of DOL compiling is the computing results of square of numbers from 0 to 19 shown in vertical order.
    
###6.Configuration Testing
    Input following codes to test whether you have configured your Ubuntu correctly:
    ---cd build/bin/main
    ---ant -f runexample.xml -Dnumber=1
