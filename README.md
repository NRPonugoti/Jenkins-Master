# Jenkins-Master
Jenkins : it is process of automating the building and testing of code , each time one of the team member commits changes to version control 
 Jenkins is an open soruce automation server written in Java , Jenkins help us to automate the non-human part of software developemnt process
 with continues integration and facilitating technical aspects of continues delivery

 Source code ---Initiate CI Process ---> build(Maven) ---->Test ---Report--->Development ----commit ---> Soruce code 
 
 Jenkins is facilitate the build and test the jobs 



 # Jenkins Master-Slave Architectire 

 Soruce code repository-----jenkis master pull the code every time when there is a commit ---> Jenkin Server(Master)
 
                                                                                                |     |       |
                                                                                                |     |       |
                                                                                      Jenkin Slave1  Slave2 Slave3


 Jenkins master distributes it workload to all the slaves 
 on request from jenkins master , the slave carry out builds and tests and produce test reports 

 When one of the Jenkins servers fails, everything fails, which is something I don't want to happen.

I don’t’ want to fail a single Jenkin server; if you fail, you need back
Work load is increasing on the Jenkins server. The amount of work should be distributed to Jenkins slaves.
Slave nodes—nothing but machines—do the work and give it back to the Jenkins server master.
Master is the one who is talking to SCM (git).

Two benefits of Jenkins master-slave architecture:

* Load distribution

* If master node crashes, then worker node will take care.

Establish the connection b/w Jenkins master and slave using ssh 
  
