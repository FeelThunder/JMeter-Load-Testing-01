# JMeter: Performance and Load Testing

## Objective
* Learn basic of how JMter works.
* Learn basic parameter in JMeter such as Thread group, Sampler, Listener, Timers.
* Learn how to run load testing through command line (CLI).
* Learn how to use Adds on.
* Learn how to show the result through Listener.
* Learn how to present the result using dashboard.

## Content 
### Command Used
- jmeter.bat
- jmeter -n -t 03_start.jmx
- jmeter -n -t 03_start.jmx -l demoresult.jtl
- jmeter -n -t 04_start.jmx -l demoresult2.jtl -e -o demoresults
 
### Plug in used
* 3 Basic Graphs	
* 5 Additional Graphs

### Load Testing 
Applying simulated load to a system and measuring the overall impact on the system

### Thread group
* A group of people waiting to do what is written in the test plan section	
* Perform actions specified in test plan
* Can run at different times and be scheduled	
* Can run multiple thread groups in one test 

### Sampler
Actions for users (threads) to perform  
Samplers within JMeter  
* HTTP Sampler	
* TCP Sampler
* LDAP Request
* JDBC Request 
* SMTP Sampler  
* Beanshell Sampler
* FTP Request
* JUnit Request
* OS Process Sampler

### Listener
Displaying the results of a test as it's running    
note: for larger tests, this isn't recommended, because displaying the output live during the load test can use a lot of system resources.      
note : Listeners let you visualize data from your load test, but the JMeter built-in listeners sometimes aren't enough.     
note : The plugins can be used during the test, however that does use a lot of resources, so it's usually better to graph the data after the test is finished.    

### Timers 
* Help introduce randomness to the test. 
* Space out actions to combat congestion. 
* Allow business logic to occur during test. 

### Running  load test through the CLI
The CLI is the purest way of running a load test.  

GUI  
* Great for creating/debugging tests 
* Uses more system resources when running tests 
CLI  
* Great for running the load tests 
* Uses less system resources to run tests 
* Allows for distribution of tests 

Parameters in command line   
* -n : switch runs in non-GUI mode
* -t : switch specifies the test file
Saving CLI results to a .jtl file  
* -l for our testing report.
Importing a .jtl file to JMeter graphs  
I've used jp@gc response codes per second and browse .jtl file  
Creating an HTML dashboard at CLI runtime  
* - e will tell JMeter to perform any action following it only after the test has completed  
* - o followed by a name to create dashboard folder  
