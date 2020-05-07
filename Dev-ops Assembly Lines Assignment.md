#Dev-ops Assembly Lines Assignment
##Objectives:-
1)	When developer commit a code while upgrading in the branch of git tool. It will send to QA Team. A testing environment is created and the upgraded code is copied there to test.
2)	If QA team found the code stable. They trigger that the code is working fine.
3)	If code is working fine then, merge the branch to master and copy it to production Environment.


 

Solution 1 –
We create a job (branch) in Jenkins which have three functions: 
a.	When developer commit a code it will push to the github with post-commit shell script. And Jenkins Monitoring the changes in the github repository using Poll SCM trigger.
b.	If found any update it will create testing environment within a second for the testing team.
c.	Copy the code from github to the testing environment.
 



 
 


Solution 2 – 
	Create job (QAT) which only triggers when the code is stable for production environment declared by QA team. 

 
 


Solution 3 –
	Create job (master) which runs only if job2 is run successfully. It will merge the code in master in the github and copy the code from github to the production environment. 
For client computer, using ngrok to view the upgraded code in browser located in public network.
 

 

 


