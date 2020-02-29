# Eureka

 ### Instructions:  
 
 
 1. Clone the repo with ```git clone https://github.com/theHubAUBGproject/Eureka.git```.  
 2. Get Django using ```pip3 install Django==3.0.3```. It's highly suggested that you do this in a venv.  
 3. You can run the test server by using:
 ```bash
 $ cd eureka
 $ python manage.py runserver
 ```
 In case you have both Python 2 and 3, you should use:  
```bash
$ python3 manage.py runserver
```

Your Python version should be at least 3.6 for this version of Django.

### Contribution Guide:

 Fork the repository and then:  
 ```
 $ git clone yourforkedcopy.git
 ```   
 Add upstream using: 
 ```
 $ git remote add upstream https://github.com/AUBGTheHUB/Eureka.git
 ```    
 To pull the most recent changes from the main repo:  
  ```
  $ git pull origin master
  ``` 
 Make your changes, do your commits and push the changes to the forked repo.
 Do a pull request against Eureka/master to request to merge your changes.


### ----- Linux Instructions for installing MongoDB -----

#####   RedHat Based Distros (Fedora, CentOS, RHEL):
```bash
$ sudo touch /etc/yum.repos.d/mongodb.repo
```
Edit the file with whatever text editor. Add this in:  
```
[mongodb-4.2]
name=MongoDB Repository
baseurl=https://repo.mongodb.org/yum/redhat/7/mongodb-org/4.2/x86_64/
gpgcheck=1
enable=1
gpgkey=https://www.mongodb.org/static/pgp/server-4.2.asc

```

#### Fedora:
```bash
$ sudo dnf install mongodb-org
```  
#### CentOS/RHEL:  
```bash
$ sudo yum install mongodb-org
```  
  
  
###   Debian Based Distros (Debian, Ubuntu, Pop! OS, Elementary OS):
```mongodb``` package provided by Ubuntu is not actually maintained by the MongoDB community. You should first uninstall that package.  

Add the MongoDB GPG key for the apt repository:  
```bash
$ wget -qO - https://www.mongodb.org/static/pgp/server-4.2.asc | sudo apt-key add -
```

If you receive an error indicating that gnupg is not installed:
```bash
$ sudo apt-get install gnupg
```
Then, retry the previous **wget** command.  
Add the MongoDB repository with:
```bash
$ echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb.list
```  

Finally, install MongoDB using:
```bash
$ sudo apt-get install mongodb-org
```
