# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise

# Linux commands-Shell scripting
Linux commands-Shell scripting

# Name : SUDHARSANAN U
# Reg.no : 212224230276

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
<img width="617" height="94" alt="image" src="https://github.com/user-attachments/assets/ca0333d6-c88c-41be-98fb-cdae9cb0f2a3" />


cat < file2
## OUTPUT
<img width="875" height="111" alt="image" src="https://github.com/user-attachments/assets/51cee7c3-c43d-48d2-b8c1-04418f46b133" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="878" height="42" alt="image" src="https://github.com/user-attachments/assets/85b84cb0-c135-4de8-b54a-6d63f532dcd0" />

comm file1 file2
 ## OUTPUT
<img width="878" height="152" alt="image" src="https://github.com/user-attachments/assets/ffa5acf2-1290-4bb1-8714-b24117ebe95e" />

 
diff file1 file2
## OUTPUT
<img width="878" height="183" alt="image" src="https://github.com/user-attachments/assets/4d2e50eb-f485-4fbf-89cf-6af52dc57893" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
<img width="878" height="61" alt="image" src="https://github.com/user-attachments/assets/95b28790-58d3-4f4d-978e-f20cf499e593" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="878" height="78" alt="image" src="https://github.com/user-attachments/assets/902bb5dc-9e93-4b6f-a43f-1a1572d234e9" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="878" height="78" alt="image" src="https://github.com/user-attachments/assets/70b78583-586a-4e50-be7f-bb3e1d9de829" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
<img width="878" height="38" alt="image" src="https://github.com/user-attachments/assets/681fe93c-73ec-48bb-ad76-7bb6b63c5629" />



grep hello newfile 
## OUTPUT
<img width="878" height="47" alt="image" src="https://github.com/user-attachments/assets/214aed1c-dda0-4955-8842-1e4de4d3a0ea" />




grep -v hello newfile 
## OUTPUT
<img width="878" height="42" alt="image" src="https://github.com/user-attachments/assets/b260b3cf-d903-4fbb-8435-e5b397408961" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="878" height="57" alt="image" src="https://github.com/user-attachments/assets/4d72ceef-6a72-4912-bda0-8b575c5b12c1" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="878" height="44" alt="Screenshot from 2026-02-09 09-03-35" src="https://github.com/user-attachments/assets/357d582c-1a92-42ff-9682-910d2e364bad" />




grep -R ubuntu /etc
## OUTPUT
<img width="878" height="58" alt="image" src="https://github.com/user-attachments/assets/8e971f4f-da18-4955-89a6-de686bd2cdd6" />



grep -w -n world newfile   
## OUTPUT


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="878" height="58" alt="image" src="https://github.com/user-attachments/assets/abc5ccd5-49b0-4cdd-a80b-9fa88d5e736b" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="878" height="58" alt="image" src="https://github.com/user-attachments/assets/587e1fa7-e778-4a2c-9b95-7333d9525488" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="878" height="58" alt="image" src="https://github.com/user-attachments/assets/f9cbbffe-8f25-492c-b2ec-bb71ab62ce52" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="878" height="42" alt="image" src="https://github.com/user-attachments/assets/7e468c63-bb25-469a-b8e1-69cc66297266" />



egrep '(world$)' newfile 
## OUTPUT
<img width="878" height="54" alt="image" src="https://github.com/user-attachments/assets/2326ef7f-bc9b-4950-97e5-ef597dd3f855" />



egrep '(World$)' newfile 
## OUTPUT
<img width="878" height="43" alt="image" src="https://github.com/user-attachments/assets/db78c6b0-fc17-4991-895c-ed343c33200b" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="878" height="77" alt="image" src="https://github.com/user-attachments/assets/584df3db-a0cc-49b4-9cbc-55e58fd2559e" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="878" height="46" alt="image" src="https://github.com/user-attachments/assets/81e4b224-7a57-4ae3-8e75-0b6444683e48" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="878" height="46" alt="image" src="https://github.com/user-attachments/assets/a1f279fa-3b40-4e82-a359-1da0bd05133b" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="878" height="46" alt="image" src="https://github.com/user-attachments/assets/f7ef4fa5-7ce8-4a02-a1c7-b9f979fe23fe" />


egrep l{2} newfile
## OUTPUT
<img width="880" height="61" alt="image" src="https://github.com/user-attachments/assets/1b8b7410-04b3-4c45-a9f5-aa35768f6acf" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="880" height="79" alt="image" src="https://github.com/user-attachments/assets/ccca724a-8f1c-4cbf-8d91-fee491879e19" />


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
<img width="880" height="47" alt="image" src="https://github.com/user-attachments/assets/7d5db18a-de66-4fc0-b282-4aa01cd4317a" />



sed -n -e '$p' file23
## OUTPUT
<img width="880" height="47" alt="image" src="https://github.com/user-attachments/assets/388c7002-be2b-4c67-810d-91721c502299" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="880" height="169" alt="image" src="https://github.com/user-attachments/assets/79946b20-3b08-44bd-ae87-107c51b41745" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="880" height="169" alt="image" src="https://github.com/user-attachments/assets/f74ac657-c56a-4b15-9ec0-9ac1a9b3ac1c" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="880" height="169" alt="image" src="https://github.com/user-attachments/assets/ae44607b-f725-4eb8-b0cc-b69d46f2c656" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="880" height="117" alt="image" src="https://github.com/user-attachments/assets/accc5802-7f4b-465c-95e0-a68bf7b689d5" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="880" height="81" alt="image" src="https://github.com/user-attachments/assets/464194cf-3b92-4233-bfe4-f7aa95cdcc1e" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="880" height="61" alt="image" src="https://github.com/user-attachments/assets/553fc830-6630-4f3e-898b-07c71402911f" />



seq 10 
## OUTPUT
<img width="880" height="201" alt="image" src="https://github.com/user-attachments/assets/a0894889-dca4-42f7-8cbc-3a1d4f89a9fd" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="880" height="80" alt="image" src="https://github.com/user-attachments/assets/96ba3876-5d18-446c-acba-fbac11329f0a" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="880" height="80" alt="image" src="https://github.com/user-attachments/assets/4992b878-0e44-4f0d-b289-ee9bd6160327" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="880" height="98" alt="image" src="https://github.com/user-attachments/assets/d64d2493-9ef8-4980-ba6f-231737d3c3f2" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="880" height="79" alt="image" src="https://github.com/user-attachments/assets/bf212cbd-e925-42ad-90d0-cb55b7f13455" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="880" height="79" alt="image" src="https://github.com/user-attachments/assets/f59c3789-4064-47f2-b09c-3d2d90774972" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="880" height="79" alt="image" src="https://github.com/user-attachments/assets/ef0b3480-eb21-4f27-92fb-d76a774ff57a" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="880" height="79" alt="image" src="https://github.com/user-attachments/assets/dd116f59-9e94-443a-89e6-5a62aa3bd396" />


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
<img width="880" height="115" alt="image" src="https://github.com/user-attachments/assets/727cd786-8444-4ecf-b2f9-cd994b8ab7f6" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
<img width="880" height="115" alt="image" src="https://github.com/user-attachments/assets/58e5edcd-b424-41cc-9d7e-407985d988f6" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="880" height="170" alt="image" src="https://github.com/user-attachments/assets/def4cc2b-c225-4b09-b8fc-21e217a8c895" />



cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="880" height="83" alt="image" src="https://github.com/user-attachments/assets/74bcdbae-343f-4f2b-942a-44cc323647fd" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="880" height="83" alt="image" src="https://github.com/user-attachments/assets/f6482e68-fd20-46dc-a734-002a17c70325" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1139" height="302" alt="image" src="https://github.com/user-attachments/assets/678858e5-8067-4086-a115-daa920e87023" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1442" height="414" alt="image" src="https://github.com/user-attachments/assets/805d2479-e431-46c6-85ea-8c0c51e77c12" />


tar -xvf backup.tar
## OUTPUT
<img width="705" height="252" alt="image" src="https://github.com/user-attachments/assets/0094e583-be48-4755-b516-b493a8c6fea6" />


gzip backup.tar

ls .gz
## OUTPUT
<img width="1043" height="423" alt="image" src="https://github.com/user-attachments/assets/18ef3624-56ee-4b80-bb0f-e065c18f9230" />

gunzip backup.tar.gz
## OUTPUT
<img width="1043" height="442" alt="image" src="https://github.com/user-attachments/assets/2b00309c-063a-49c8-b238-d807e52c13d2" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="831" height="183" alt="image" src="https://github.com/user-attachments/assets/08abf373-8eee-4d04-b52b-e1987008fa07" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="710" height="81" alt="image" src="https://github.com/user-attachments/assets/e47cc869-2784-4bb9-800f-d56887cf6dd9" />


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
<img width="1039" height="756" alt="image" src="https://github.com/user-attachments/assets/920460f1-c224-4247-a097-3a209f1452f4" />
 
ls file1
## OUTPUT
<img width="1039" height="37" alt="image" src="https://github.com/user-attachments/assets/e3101854-9649-4dd3-ae46-38aeb15d6c5b" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
<img width="1039" height="46" alt="image" src="https://github.com/user-attachments/assets/50e09a22-1729-4ce6-9ff2-8e7870083ef4" />

 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
## OUTPUT
<img width="1052" height="404" alt="image" src="https://github.com/user-attachments/assets/d7df5688-5de4-49f8-92c1-45fed24c6643" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="1052" height="78" alt="image" src="https://github.com/user-attachments/assets/01062a96-c262-427c-91dd-b12465435039" />


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
<img width="1052" height="330" alt="image" src="https://github.com/user-attachments/assets/2e299826-2f58-465d-accc-6937c8eb556a" />

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
<img width="1047" height="644" alt="image" src="https://github.com/user-attachments/assets/c79565b1-fc49-484c-a41e-68c65f964a2a" />
<img width="1047" height="111" alt="image" src="https://github.com/user-attachments/assets/e5459641-18ff-439f-b150-f282b255a858" />



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
## OUTPUT
<img width="1047" height="653" alt="image" src="https://github.com/user-attachments/assets/0e8a4c35-820b-48de-a9ae-204201a66591" />


# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
## OUTPUT
<img width="1047" height="644" alt="image" src="https://github.com/user-attachments/assets/c79565b1-fc49-484c-a41e-68c65f964a2a" />
<img width="1047" height="111" alt="image" src="https://github.com/user-attachments/assets/e5459641-18ff-439f-b150-f282b255a858" />

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
<img width="1047" height="415" alt="image" src="https://github.com/user-attachments/assets/70a1ddb9-27c0-4a74-bb0e-6e023574b541" />

# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
<img width="1047" height="225" alt="image" src="https://github.com/user-attachments/assets/ba3013df-f148-487b-acd6-7bee96229859" />


# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
## OUTPUT
<img width="1047" height="277" alt="image" src="https://github.com/user-attachments/assets/9db60204-48ef-4457-b3ee-1eb2f15c9ead" />

 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
## OUTPUT
<img width="1047" height="417" alt="image" src="https://github.com/user-attachments/assets/33715f44-73f9-45f7-a9f7-f31d2755d60f" />

cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
## OUTPUT
<img width="1047" height="273" alt="image" src="https://github.com/user-attachments/assets/0ae30fcf-13d0-4d02-96b7-41e3d4aa09e5" />

 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
## OUTPUT
<img width="1047" height="311" alt="image" src="https://github.com/user-attachments/assets/f9124b74-db21-4c3a-8276-3e404420d136" />

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh
## OUTPUT
<img width="1047" height="255" alt="image" src="https://github.com/user-attachments/assets/dd9402a0-1454-48be-bf7d-3b6cce3b8786" />

cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
## OUTPUT
<img width="1047" height="307" alt="image" src="https://github.com/user-attachments/assets/a7e900f3-8b3c-4215-b44c-418b07f5c7b9" />

cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
<img width="1047" height="311" alt="image" src="https://github.com/user-attachments/assets/f9124b74-db21-4c3a-8276-3e404420d136" />

cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
<img width="831" height="257" alt="image" src="https://github.com/user-attachments/assets/87cc725f-db95-4244-91f7-7092a1d5773c" />


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
<img width="1047" height="256" alt="image" src="https://github.com/user-attachments/assets/09b5f94a-9f5f-428d-bfeb-c83f611311d8" />

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
<img width="1047" height="256" alt="image" src="https://github.com/user-attachments/assets/dc576266-751c-4b81-b2a7-b5445fa0a510" />

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
<img width="1047" height="457" alt="image" src="https://github.com/user-attachments/assets/6cd19038-054c-4a7f-9b61-cc60db266b79" />

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
## OUTPUT
<img width="1047" height="726" alt="image" src="https://github.com/user-attachments/assets/bfbfe36c-0a4c-4e04-ba8b-14b453be6ad5" />

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
<img width="1047" height="726" alt="image" src="https://github.com/user-attachments/assets/bfbfe36c-0a4c-4e04-ba8b-14b453be6ad5" />

cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
<img width="1047" height="189" alt="image" src="https://github.com/user-attachments/assets/e0b23361-4a73-4408-b9c2-29974328262b" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 

## OUTPUT
<img width="1047" height="236" alt="image" src="https://github.com/user-attachments/assets/7f711c91-44fc-4fca-90fa-5f52a3f4440a" />

 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
./funcex.sh 
./funcex.sh 1 2


## OUTPUT
<img width="1047" height="329" alt="image" src="https://github.com/user-attachments/assets/02799d55-6cbc-41f7-a0f1-50529679e6e8" />

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3

## OUTPUT
<img width="1047" height="207" alt="image" src="https://github.com/user-attachments/assets/2096cb78-e998-436b-96fc-9e9bceeb317e" />

 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3

## OUTPUT
<img width="1047" height="291" alt="image" src="https://github.com/user-attachments/assets/8169d119-3cc6-4b62-9cc6-55cd78190bc9" />

cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
 \./argshift.sh 1 2 3

## OUTPUT
<img width="1047" height="418" alt="image" src="https://github.com/user-attachments/assets/a070798e-65fc-4615-a3db-175004623028" />

 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
<img width="1392" height="668" alt="image" src="https://github.com/user-attachments/assets/2f3ced1f-1e6c-4559-b2f4-daa60d6aec26" />

cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
<img width="1392" height="531" alt="image" src="https://github.com/user-attachments/assets/8ab3c65a-4b71-4ee2-997a-93d27f2db70c" />


# RESULT:
The Commands are executed successfully.
