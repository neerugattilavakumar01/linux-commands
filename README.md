# linux-commands
linux-commands
1. ONE TIER
2. TWO TIER
3. THREE TIER
4. N TIER

TIER = LAYER = SERVE

LAYERS: 3 TYPES

1. PRESENTATION LAYER:

# TO SEE THE APPLICATION.
# IT IS ALSO CALLED AS CLIENT LAYER. (CLIENT=END USERS)
# IT IS TOP LAYER OF AN APPLICATION.
# PRESENTATION LAYER COMMUNICATES WITH APPLICATION LAYER.


2. APPLICATION LAYER:

# TO USE THE APPLICATION.
# IT IS ALSO CALLED AS LOGIC LAYER.
# IT IS THE MIDDLE LAYER.
# APPLICATION LAYER COMMUNICATE WITH BOTH PRESENTATION AND DATABASE LAYER.

3. DATABASE LAYER:

# TO STORE AND RETRIEVE DATA.
# IT IS ALSO CALLED AS DATA LAYER.
# IT IS LAST LAYER.
# IT WILL COMMINCATE WITH APPLICATION LAYER.


1. ONE TIER ARCHITECTURE:
WE CAN CREATE ONE-TIER APPLICATION (STAND-ALONE APPLICATION)

EX: VLC MEDIA PLAYER

THE PRESENTATION, APPLICATION AND DATABASE LAYER WILL BE ON A SINGLE SIDE.
NOTE: We don't need internet.

2. TWO-TIER ARCHITECTURE:
WE CAN CREATE TWO-TIER APPLICATIONS (CLIENT-SERVER)

EX: JIO SAAVAN

CLIENT-SIDE: PRESENTATION, APPLICATION
SERVER-SIDE: DATABASE LAYER

NOTE: WE NEED THE INTERNET, HERE APP NEED TO BE ON LOCAL DEVICE.

3. THREE-TIER ARCHITECTURE
WE CAN CREATE WEB-APPLICATIONS 

EX: YOUTUBE

CLIENT SIDE: PRESENTATION LAYER
APP SIDE   : APPLICATION LAYER
DB SIDE	   : DATA BASE LAYER

NOTE: WE NEED NOT TO DOWNLOAD APP ON LOCAL DEVICE
WE CAN ACCESS THE APP FROM INTERNET.

4. N-TIER:
DISTRIBUTED APPLICATIONS

HERE WE HAVE MORE THAN ONE SERVER ON THE APPLICATION.



COURSE: DEVOPS WITH AWS
DURATION: 2.5 MONTHS
FEE: 8k 
TIMINGS: 6 - 7:30 PM
HANDSON: 
TOOLS: 11 TOOLS
AWS: 10

EXP: 3 YEARS
CONTENT: 


https://github.com/RAHAMSHAIK007/handsonsyllabus

=====================================================================================
SERVERS:
Serves the services to the end users.
To host the application. 


TYPES: 
1. WEB SERVER: PRESENTATION LAYER	: TO SEE THE APP
2. APP SERVER: APPLICATION LAYER	: TO USE THE APP
3. DB SERVER: DATABASE LAYER		: TO STORE & RETRIEVE DATA


ON-PREM: PHYSICAL SERVERS
CLOUD SERVERS: SERVERS WHICH ARE CREATED ON DATA CENTERS.

AWS -- > SERVER -- > EC2 INSTANCE
EC2: ELASTIC COMPUTE CLOUD.

AGENDA -- > CREATE A SERVER & HOST NETFLIX APPLICATION

TO CREATE A SERVER WE HAVE 7 STEPS:
ASSUME SERVER = COMPUTER

1. TAGS = NAME 
2. AMI(AMAZON MACHINE IMAGE) = OS, SOFTWARES
3. INSTANCE TYPE = RAM, CPU
4. KEYPAIR = LOGIN TO SERVER (PEM & PPK) [public: aws, private: user]
5. NETWORK = VPC, SECURITY GROUPS (0-65,535)
6. STORAGE = EBS VOLUME (min=8 Gb, max=16 TB)
7. SUMMARY = REVIEW & LAUNCH 

SECURITY GROUPS: TO ALLOW AND RESTRICT THE TRAFFIC.
TRAFFIC = INCOMING REQUEST AND OUTGOING RESPONSE


CONNECT TO SERVER -- > CLICK ON CHECK BOX -- > CONNECT -- > CONNECT

APACHE SERVER -- > TO SHOW THE APPLICATION 
WEB SERVER:
It is used to show the application.
ex: apache, nginx 
port: 80 

#install apache(web server) git(code)
yum install httpd git -y

#start the web server
systemctl start httpd
systemctl status httpd

#insert the code on default path of apache
cd /var/www/html
git clone https://github.com/CleverProgrammers/pwj-netflix-clone.git
mv pwj-netflix-clone/* .

NOTE: For all free and open-source better to prefer n-1 version.


DIS ADVANTAGES OF WINDOWS:
1. HANG
2. PAID
3. NOT MULTI-USER BASED
4. NOT SUPPORTING FOR MULTI-TASKING


WHY LINUX 
LINUX IS A FREE AND OPENSOURCE OS
LINUX SYSTEMS WILL NOT NOT HANG FREQUENTLY.
IT IS A MULTI-USER-BASED OS
IT WILL SUPPORTED FOR MULTI-TASKING


WHAT IS LINUX 
IT IS A FREE AND OPEN-SOURCE OS.

OPERATION SYSTEM: Its used for communication blw user and system.
OPEN-SOURCE: We can see the code, change the code and distribute the code.

Linux torvalds invented the linux with c language.
linux comes in market 1991.

FLAVORS/DISTRIBUTIONS:

IPHONE: MINI, PLUS, PRO, PROMAX 
LINUX: REDHAT, CENTOS, FEDORA, AMAZONLINUX, UBUTNU, DEBIAN 

DOWNLOAD LINUX: NOT REQ

WHERE: 
ANDROID
SMART WATCHES, TV
SERVERS
SUPER COMPUTERS (500/500)

=================================================
STEP-1: USER EMAIL, NAME & CODE AND PASSWORD
STEP-2: Contact Information 
STEP-3: Billing Information 
STEP-4: VERIFY CONTACT 


LINUX COMMANDS: 

MODES OF LINUX:
GUI: GRAPHIC USER INTERFACE
CLI: COMMAND LINE INTERFACE

By default we login with ec2-user 
but in real we work with root user.
(ec2-user: default root=admin)



sudo -i: to switch to root user
clear/ ctlr l: to clear the screen
touch file1: to create a file
ls/ll: to list the files
cat file: to show content in file1
cat>>file1: to insert content in file1
ctrl d: to save the content
cp file1 file2: to copy the content from file1 to file2
mv file1 raham: to rename file to raham
rm file1: to remove the file1
rm file2 -f: to remove file2 forcefully
touch file{1..10}: to create file1 to file10
rm * -f: to remove all files forcefully
rm j* -f: to remove all files starting with j
rm p* -f: to remove all files starting with p


head file1: shows first 10 lines
head -5 file1: it shows first 5 lines
head -12 file1: it shows first 12 lines	
tail file1: shows bottom 10 lines
tail -5 file1: it shows bottom 5 lines
tail -12 file1: it shows bottom 12 lines	

sed -n '5,15p' file1: to pint line 5 to 15

========================================================

DAY-02:

PERMISSIONS:
-    rw-r--r-- 1 root root 0 Aug  9 12:51 raham

TYPE OF FILES IN LINUX:
-	: regular file
b	: blocked file
c	: charcter file
d	: directory (folder)
l	: linked file

PERMISSIONS:

READ	: r	: 4
WRITE	: w	: 2
EXECUTABLE: x	: 1

PARTS:
USER: rw : 6
GROUP: r : 4
OTHERS: r : 4


M-1: chmod 777 filename
M-2: chmod u=rw,g=rwx,o=x raham
M-3: chmod -r raham 


USERS & GROUPS:
WHY TO CREATE USERS: In real time if we want to work with servers we need to have user and password to login .

server -- > user & password

useradd raham	: to create user
cat /etc/passwd : to list users
getent passwd   : to list users
passwd raham	: to give password
su - raham	: to login as raham users
ctrl d		: to logout form raham user

NOTE:
username should not password
length must be 8 charc
password will not be visible.

user = group & folder will created

cat /etc/group: to list group
getent group: to list group
ls /home
userdel revi

if we del user group will go but not the folder.

chown raham:raham filename 

chown means change ownership
we use this command to change the user

====================================================

EDITORS: To edit and add the content in a file.
TYPES:
1. VIM/VI
2. NANO

i to insert the conetnt
esc to get back


1. command mode
2. insert mode
3. save mode

SAVE MODE:
:w	: save
:q 	: quit
:wq	: save & quit
:wq!	: save & quit forecfully
INSERT MODE:
i	: to insert the content
I	: starting of line
A	: Ending of line
O	: Create new line above existing
o	: Create new line below existing

COMMAND MODE
gg	: top of file
shift g	: bottom of file
yy	: copies single line
3yy	: copies 3 lines
p	: paste single time
3p	: paste 3 times
dd	: delete single line
10dd	: deletes 10 lines
u	: to undo
:15	: goes to line 15
:25	: goes to line 25
:set number: to print line numbers
/word	: to search for a word inside a file

GREP: To search the words outside a file
grep word file1 	: to search for word in file1
grep word file1 -i	: to search for word in file1 (to avoid casesensitive)
grep 'word1\|word2' file1 -i : to search multiple words
grep word file1 -i -v	: -v to aviod the word
cat file1 | grep raham -i

HARWARE COMMANDS:
lscpu: to show cpu info (cat /proc/cpuinfo)
lsmem: to show RAM info (cat /proc/meminfo)
fdisk -l: to show rom (df/df -h/df -m)
uname: to print os
cat /etc/os-release: to show flavor

==============================================

SED: stream editor
to replace the word in a file.

inside of file - :%s/word1/word2/

outside of file - 
sed 's/ravi/raju/' file1 >> file2
sed 's/ravi/raju/;s/is/are/' file1 >> file3
sed '2c hai all' file1



=====================================================================

ADVANCE COMMANDS:

scenario-1: what u will do when the server runs slowly?

1. check the cpu & memory utilization. (top)
   yum install htop -y 

2. check the instance checks 
   we need to restart the server.

scenario-2: how u can check active ports for the server
netstat 

scenario-3: how to check the process in Linux
how will you check your app is running inside the server

ps -ef
ps aux
ps -ef | grep 80

to kill process: kill -9 pid
