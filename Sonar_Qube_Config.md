SonarQube is an open platform to manage code quality ,As such , it covers the 7axe of code quality 


SonarQube :
create linx machine and  install all required documents 
CREATE THE EC2 MACHINE WITH T2.MEDIUM 
SONARQUEBE DEFAULT PORT :9000
OPEN THE PORT IN EC2 

then go to root  user of VM Machine 
#adduser sonarquebe 
switch to user 
#sudo su - sonarquebe
then 
#yum install java-1.8*  -y
then
#cd /opt
download sonarquebe 
#wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-6.7.7.zip
then go to root user 
install unzip 
#yum install unzip 
go back to sonarquebe user 
#sudo su - sonarquebe
then unzip 
#unzip 
then 
#chmod -R 755 /home/sonarqube/sonarqube-9.4.0
#chown -R sonarquebe:sonarquebe /home/sonarqube/sonarqube-9.4.0

#cd /opt/sonarqube-7.8/bin/linux-x86-64
then start sonar 
#sh sonar.sh start

sonar running port :9000
publicip:9000
default user name and password 
admin
admin
create new password 
now jenkins and sonarqube both are dirrent and how to communicate it 
go to sonarqube -----> click my account ---> click security----> generate tokens : jenkins click generate 
copy the tokne save it 

install sonar qube plugin in jenkins 

mange jenkins--->Plugin manager---->avaiable --->Sonar Qube Scanner----> instal it 

go to jenkins  --- manage jenkins ------ credentails -------systems --global credentail ----add credentail ---kind: screet text 
secret: provide token of sonarqube 
id: sonarqube 
save it 

then 

Manage Jenkiins----> COnfigure Systems 
                    serverName: sonar-server
                    ServerUrl: url of sonar qube 
                    server Authentication tokens: sonarqube


then Apply and Save it 

Manage Jenkins -----> GLobal tool configuration ------> SonarQube Scanner 
                    Name: sonar-scanner
                   version: SonarQube Scanner 4.8
apply and save it 



