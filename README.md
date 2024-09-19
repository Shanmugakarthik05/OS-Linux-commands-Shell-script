# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

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
![image](https://github.com/user-attachments/assets/b84ef6e9-d23c-444a-972b-92fcbd4fa0a2)

cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/bbbf3aff-8b2f-41cc-b4df-07363a8a2ca1)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/user-attachments/assets/5248917b-7b97-4d84-b9db-112c7a4cf303)

comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/bb9e59d7-dc2c-4c59-8b0f-6db780bb56aa)

 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/259e87a1-8678-414f-aeb0-f6a42c0a6d23)


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
![image](https://github.com/user-attachments/assets/91e3a9ec-523c-416c-b969-818238060a65)


cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/fa4608dc-4fbb-451f-989a-cf99dc02e8db)


cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/901eed77-dfcb-43b2-93b5-3cd0bd7dc7ca)


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
![image](https://github.com/user-attachments/assets/d70f1b2d-66c7-4e6f-b892-59d1561b034f)

grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/73e2cc38-4eca-4fdb-881f-5e8510ba4c14)


grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/e0e66bed-81ac-49b6-8cfc-ada5d0c74c74)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/5641de94-726c-40b9-83d7-fc9c5874d78f)

cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/207d49d8-3ce8-403a-93c6-05061ade1579)


grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/user-attachments/assets/b7683a1e-2eee-4e72-a786-1c1f9a0267b5)


grep -w -n world newfile   
## OUTPUT

![image](https://github.com/user-attachments/assets/be2f6694-9bd2-4f2f-bf3d-8a4b7386d00d)

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

![image](https://github.com/user-attachments/assets/5b4bd9de-c196-49f6-b2fb-7cbc3a804b97)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/e946bdf7-7994-47c8-8341-98d6da799f80)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/2675841e-6ab6-47aa-a82f-6435f0a91d3c)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/d7a43c59-b1a8-480d-b708-358175be3d48)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/93843bcd-86f8-49b0-b82c-46ad20fd458b)


egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/ed8dbfd2-6107-426c-aad6-95e6a8a3294c)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/b54337bb-63df-419a-bb3a-34a7c9a82244)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/c17f237e-fee3-4a17-8cbe-ae1a05203e52)


egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/cdeba6d7-8d36-47be-b5de-8dbbabd24797)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/3e039a5b-927b-4625-9ef0-80c1a677cb51)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/4a73ae3d-392c-4c67-a825-96dd3776eb94)


egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/3e33af74-6c36-43f1-8f62-8db19e940320)


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

![image](https://github.com/user-attachments/assets/21762888-e8fc-4beb-af23-f5309e38e177)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/aa91e6b2-507b-4e21-8e5f-35b8ec84f188)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/030d5140-6bc2-4754-9529-744ca43ce8b9)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/ef6d270a-a519-4012-922c-412decbfa0e5)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/b6aa394d-c10c-4c4d-920e-1197a50c17d1)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/bf09cd0b-d1bc-406b-b8e8-dc04703c1db4)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/7eee8bc1-475a-43a6-98d5-0ddf2d390d3f)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/f82cf5db-1348-4e7f-b296-009592dd9b6d)


seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/2e14adcb-a1be-4824-9e18-6d6b495aa11e)


seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/user-attachments/assets/3a98582d-13d0-49c4-8e9e-d091e61737a0)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/user-attachments/assets/28df880d-60bd-4306-b8cc-0c95440a6166)


seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/630f7407-91f2-430c-9bb3-3589afbff2c9)


seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/16f6ca60-197f-41e3-9bbf-98503eb8c2c5)


seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/9bdf4f8a-83c5-4b9f-bed7-1268a6cdf67e)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev


sed -n '2,4{s/$/*/;p}' file23


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
![image](https://github.com/user-attachments/assets/41867fc0-6287-4a75-afdc-ec3cadf3c43d)


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
![image](https://github.com/user-attachments/assets/0f0506ee-4e3b-42bf-96f9-3fb3e27e5b6a)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/0e27da5a-96fe-454d-9924-e32bb4e92e8f)

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

![image](https://github.com/user-attachments/assets/d1903f31-81a9-4c03-8154-3b6583d711c7)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/user-attachments/assets/6b405fc5-4d1a-4c25-b5a1-af203626c60e)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/09aea32a-ce92-4166-9869-4bb5550f4080)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/ddbdcac4-9434-446e-a8c8-db6cb991f594)

tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/9901bb06-b862-4177-a585-e0bb88d7dd8e)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/user-attachments/assets/9ebaab2e-cbff-4088-a2cb-b1f5201e25c0)

gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/24425d25-0a47-46c9-936e-dd04826b77ca)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/a52bf19e-7964-49e8-89dc-dc22125d0c48)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/user-attachments/assets/264b8c87-16d2-40b2-9578-b99590e4a6d5)

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
![image](https://github.com/user-attachments/assets/a76d047f-55a8-42d9-9acf-ddcf17dcee62)

 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/4b923b8f-1ee8-44bd-8c5b-76d3d19e35bb)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/0ed30a53-12d8-4df7-991d-b2ddfb7a6e39)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
abcd
 
echo $?
 ## OUTPUT

![image](https://github.com/user-attachments/assets/af256a7c-30e0-4e42-b3b3-2a2c06b3dd71)

 
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
![image](https://github.com/user-attachments/assets/4cfa2442-419b-4f61-8ac9-250dae18cf96)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/1ad667a4-1cac-4c39-a488-d461df91929f)

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
![image](https://github.com/user-attachments/assets/a04e6ee0-ac74-493f-8820-4313a94c04b4)
	
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

![image](https://github.com/user-attachments/assets/e0694fe9-33fa-4182-bfe4-fba06b456e2b)


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
![image](https://github.com/user-attachments/assets/750011fa-2807-49ad-9703-8e249d16cfc7)

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
![image](https://github.com/user-attachments/assets/81b07374-be99-489b-86bf-14fa4d96569b)

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
![image](https://github.com/user-attachments/assets/c1942cfb-ea79-44a2-9240-08a35d2f5e18)


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
![image](https://github.com/user-attachments/assets/a88cc263-2e1b-4971-9fca-69dbf3648dfd)

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
 ## output
 ![image](https://github.com/user-attachments/assets/5c415364-af3f-4442-9428-e5eb3ee636be)

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
 ## output
 ![image](https://github.com/user-attachments/assets/00a9976e-3f34-4d7f-9075-ca89891822cd)

 
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
 ## output
 ![image](https://github.com/user-attachments/assets/c787dc0e-29f8-4ea5-bd63-a12ea1e218c3)

 
 
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
 ## output
 ![image](https://github.com/user-attachments/assets/b7055944-c492-4bdf-8dd7-07cc1477bd3c)

 
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
 ## output
 ![image](https://github.com/user-attachments/assets/95afb3b9-e024-4984-b02a-f5ae6f3725cd)

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
![image](https://github.com/user-attachments/assets/510d02ca-4454-4e60-8b1d-94177767d3c1)

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
![image](https://github.com/user-attachments/assets/791e973d-49fd-429a-8101-8a81838136f0)


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
![image](https://github.com/user-attachments/assets/3959f740-f818-499b-802a-c292920e0fdc)

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
![image](https://github.com/user-attachments/assets/16a8af2a-02d6-4f14-bfb3-6cc76cbeeeb8)

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
![image](https://github.com/user-attachments/assets/ef28431a-a1b1-48b2-893a-38a72e9b85b2)

 
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
## OUTPUT
![image](https://github.com/user-attachments/assets/6bff8926-167e-4e16-b4ff-13d65169fb36)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
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
 ![image](https://github.com/user-attachments/assets/55350faf-8b44-48ac-ab80-429229d71fda)

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

![image](https://github.com/user-attachments/assets/e2d6d9a9-af24-4636-a456-4a82101bd3a9)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 
 
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
## OUTPUT
![image](https://github.com/user-attachments/assets/8a38c3c3-2c9a-4cc2-8da0-0d8bc62c4aa1)

 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
![image](https://github.com/user-attachments/assets/80a54eb4-0169-4581-b7a3-84de68684455)

$ ./argshift.sh 1 2 3
 
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
## OUTPUT
![image](https://github.com/user-attachments/assets/970ffb03-35fe-4440-905e-5040c5dd6327)

$ ./argshift.sh 1 2 3
 
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
## OUTPUT
![image](https://github.com/user-attachments/assets/d1caf5aa-8909-4530-9ebb-08de409dfc07)


 ./argshift.sh 1 2 3
 
 
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
 ![image](https://github.com/user-attachments/assets/10a09eec-19e9-44ff-b453-5478e869d453)

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
![image](https://github.com/user-attachments/assets/7fdf2282-1ade-4ee5-a680-73af3984a39e)


# RESULT:
The Commands are executed successfully.
