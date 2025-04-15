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
![image](https://github.com/user-attachments/assets/9948a726-b5e1-471c-9f51-44662280294b)

## OUTPUT

![433027268-2a74f2f6-4b2a-45cf-a33c-302e4d4774df](https://github.com/user-attachments/assets/a4385846-b1df-4ce1-a472-4ca70fb097e4)

![image](https://github.com/user-attachments/assets/5cb4da15-f9df-456a-8238-447f5bef3f48)

cat < file2
## OUTPUT
![433027596-f6b8823c-22a9-4f1d-860f-658cd21aa2a6](https://github.com/user-attachments/assets/d370790e-b8f6-4fc3-8681-4baca41dbf19)


# Comparing Files
cmp file1 file2
## OUTPUT
![420564378-138f89a4-db43-4eef-8899-f52635967e42](https://github.com/user-attachments/assets/9230fa0a-efb5-4fd4-8a6d-154f6a7887d0)

 
comm file1 file2
 ## OUTPUT
 
![420564571-90da3e70-edd6-48eb-b4cf-c2ad17db83a3](https://github.com/user-attachments/assets/e389dc38-4704-4ae1-b898-d47266379bd7)

 
diff file1 file2
## OUTPUT

![420564671-2cdb69f4-d19b-4b76-97e9-cde88fca01cf](https://github.com/user-attachments/assets/55a47b9e-981a-44d4-b248-199f0479d6d0)

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

![420565473-6be8a211-bba1-4d9e-a72c-ce495503524a](https://github.com/user-attachments/assets/56fd51c6-c781-48e0-94aa-f61dfa5e05a2)



cut -d "|" -f 1 file22
## OUTPUT

![420565633-3bdd1090-9475-40b7-b50c-c15c184dee84](https://github.com/user-attachments/assets/d0c92059-c74e-4507-85a8-17fcbc535881)


cut -d "|" -f 2 file22
## OUTPUT
![420565555-b407a84a-aedb-45fc-aac7-a3424dd93a67](https://github.com/user-attachments/assets/a49e4a9b-bf68-4167-847b-f25fe9f8cadb)


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

![420565901-9634ae40-3cfc-41b3-a04e-5147227b2a9f](https://github.com/user-attachments/assets/5983acd2-79d2-4027-a4ad-f21c782de2ec)


grep hello newfile 
## OUTPUT

![420565982-3c71eb79-44f9-41e7-8c6d-1c1e7d2bc88b](https://github.com/user-attachments/assets/e1761f4c-50f8-4e9a-b68d-b7e530b3138c)



grep -v hello newfile 
## OUTPUT

![420566105-c7150c19-d2d3-4ba6-b529-e5d0d9bb2b5c](https://github.com/user-attachments/assets/e019f3db-8895-4997-895a-bfea869c1705)


cat newfile | grep -i "hello"
## OUTPUT

![420566273-1de4941b-12ff-42b5-8304-13ee0b2e7f26](https://github.com/user-attachments/assets/78603833-a979-4901-bca5-2422a55c01cd)



cat newfile | grep -i -c "hello"
## OUTPUT

![420566181-1c4ae9b0-18c7-43e6-be2e-2af7d8a13b07](https://github.com/user-attachments/assets/86b5f922-c18b-49a0-a37a-519933ba69e6)



grep -R ubuntu /etc
## OUTPUT



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



egrep -w '(H|h)ello' newfile 
## OUTPUT

![433033700-242a7ff4-8afb-4c67-8113-e4be317183b0](https://github.com/user-attachments/assets/f62c1ad2-3d9a-47ea-9ec4-7e4817685db7)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![433033719-93af6a85-1819-4036-a8d8-3d015333ca23](https://github.com/user-attachments/assets/f8317f8b-fd9e-4e50-8e57-d9bfc7ddf568)



egrep '(^hello)' newfile 
## OUTPUT

![433033741-6ac55ef3-aced-4258-a282-613cb393041e](https://github.com/user-attachments/assets/53d23577-26a9-4862-baf5-77631341d1a6)


egrep '(world$)' newfile 
## OUTPUT

![433033755-6e3ecc4d-4b7e-42fa-a74c-200dbf44b7f3](https://github.com/user-attachments/assets/74595cd1-13a9-4eda-a4e7-ceb5f6a4b69a)


egrep '(World$)' newfile 
## OUTPUT
![433033788-c99c0d21-c8e4-45b1-a393-86bf38fdcf0d](https://github.com/user-attachments/assets/871b5551-4b67-4d86-9c51-e7f7aab22da6)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![433033796-78ab0e42-d385-4ba9-a34a-bdfd10f6b82e](https://github.com/user-attachments/assets/29e7048d-0c08-451c-97e6-fe593de1295f)


egrep '[1-9]' newfile 
## OUTPUT

![433033829-ce48f5d8-bff6-41cc-b78a-8b0cdff177d8](https://github.com/user-attachments/assets/8faee063-2a0e-4d73-9308-0ac35a426711)


egrep 'Linux.*world' newfile 
## OUTPUT
![433033862-b12642c7-21ef-4c37-ac60-79ee7fb58662](https://github.com/user-attachments/assets/e5adf09d-a34e-4399-bbaa-5ae01abd7a7f)


egrep 'Linux.*World' newfile 
## OUTPUT
![433033871-1178900d-f6b1-4d87-b34e-46269da45872](https://github.com/user-attachments/assets/c0b7d538-594b-4864-82d6-61a9d0f8a8e3)


egrep l{2} newfile
## OUTPUT

![433033892-c69df5d6-4851-4bdc-a867-2ed609bbb31a](https://github.com/user-attachments/assets/c559613b-9f3c-4cd5-81a4-7ad578881993)


egrep 's{1,2}' newfile
## OUTPUT 
![433033906-8f5aab7b-1c60-4b21-9e06-b77a4564985f](https://github.com/user-attachments/assets/82406b70-1e34-426f-b8d7-6661c7f0cbe4)


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
![433054120-bfa9f600-6896-47fe-ba5c-72891e506c0c](https://github.com/user-attachments/assets/c291dbbb-aaed-4a8b-96e0-275c78b45316)



sed -n -e '$p' file23
## OUTPUT

![433054118-49e60597-10c3-4f07-92d0-31d71c5a5941](https://github.com/user-attachments/assets/7d2bfe25-b88e-4d26-8996-247a3befb9a7)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![433054114-aebe71fe-52e2-4517-a37f-d43268e428fa](https://github.com/user-attachments/assets/efae31c0-a3f9-45bf-9f0d-6ff465b9a6b3)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![433054078-23156dc5-9a08-4261-bcef-91a62b710ea3](https://github.com/user-attachments/assets/dc94b82a-26de-485d-bbd2-aa14b3927155)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![433054071-e06e6006-ae4c-4ce7-a199-5ec5c47ea46b](https://github.com/user-attachments/assets/079b565d-08a8-4d98-94fa-f69e1c31d386)



sed -n -e '1,5p' file23
## OUTPUT

![433054065-acbb2779-fdd9-4524-a4f4-a728efd771e4](https://github.com/user-attachments/assets/f59174fe-31ef-4851-b53b-dadea64f0f94)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![433054058-0ed77c65-f1be-49be-a26d-7428db7ceef0](https://github.com/user-attachments/assets/49a35ac9-5935-4266-a2d2-b848304ea0d3)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![433054055-099a3d38-e6f0-4ebb-9817-ff42234ed993](https://github.com/user-attachments/assets/bd8cdc7a-3bf4-4a56-b53a-bce15bb216c4)



seq 10 
## OUTPUT


![433054048-a68bf9db-b7c2-429b-9805-f6b4700ab98c](https://github.com/user-attachments/assets/43d7702a-09c1-40c3-8769-25c15b203067)

seq 10 | sed -n '4,6p'
## OUTPUT

![433054043-0515eb1f-df9a-4222-9d50-831233f2dcdb](https://github.com/user-attachments/assets/4fb58a89-4f36-46b6-ab7d-40e6475bd092)


seq 10 | sed -n '2,~4p'
## OUTPUT
![433054035-5e20bcb2-7ecd-43fe-8eb6-ee9262a00438](https://github.com/user-attachments/assets/b2ffd26c-a30e-403b-b726-31a3b94e57e3)



seq 3 | sed '2a hello'
## OUTPUT

![433054032-0afe3433-709a-4a57-9e52-e411c2a671a9](https://github.com/user-attachments/assets/47269588-fd66-43e3-89ae-3867b7ba3dba)


seq 2 | sed '2i hello'
## OUTPUT
![433054026-96ddbf03-f7ff-45b0-9790-d26cd2c62cf2](https://github.com/user-attachments/assets/1737ed8f-739d-4336-8464-177a32f73bf1)


seq 10 | sed '2,9c hello'
## OUTPUT
![433054019-911203b1-0df8-4fad-b914-65bd05901753](https://github.com/user-attachments/assets/fab79260-4ca8-410d-a8b8-cc8171664011)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![433054016-08121726-12ca-45f7-8d88-76178516a62c](https://github.com/user-attachments/assets/4aab13f6-6834-47b1-a589-b34435f91e3a)


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

![433054289-733360f2-0cc8-4564-9433-2997e038a157](https://github.com/user-attachments/assets/406dd6f9-150c-40c0-9f0a-f9f458edd3ec)

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

![433054301-208598fe-93f3-4c9b-a1c2-c70783c4bc28](https://github.com/user-attachments/assets/b2a72f06-d197-4d69-b895-892d68187919)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![433054303-51efaa25-32ec-41c7-857a-c387757e9b35](https://github.com/user-attachments/assets/c9f8688e-e29d-42ae-a821-fa03fa7eec05)

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
![433054307-1e376c3b-9666-4680-af6d-af63d554363e](https://github.com/user-attachments/assets/77c067c8-becf-4576-b16b-72386a4febe0)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![433054312-8e6a575e-3667-45a0-a5c3-0422e71e5186](https://github.com/user-attachments/assets/5f8b9a55-a2d9-406e-8c2c-21740c08cd8a)




#Backup commands
tar -cvf backup.tar *
## OUTPUT
![433054312-8e6a575e-3667-45a0-a5c3-0422e71e5186](https://github.com/user-attachments/assets/d271d8ae-08cf-4b59-9e37-8cfcd88c66ae)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![433054325-31f31183-6c34-4bf6-a97e-6c3c16f7e8a1](https://github.com/user-attachments/assets/4149ad1e-ca84-434a-8ede-634ed467bd4e)


tar -xvf backup.tar
## OUTPUT

![433054328-eef9f4b6-f0d8-44df-8176-809ac3626285](https://github.com/user-attachments/assets/56885421-26c4-41a6-a0cf-3f5e9ce6e4ed)


gzip backup.tar

ls .gz
## OUTPUT

![433054491-204f2c7b-e139-429e-aafb-980fef3a4c3a](https://github.com/user-attachments/assets/492ab561-af5c-476a-b2e4-b8a9562392f5)

 
gunzip backup.tar.gz
## OUTPUT

 ![433054496-1fa53ed1-70d5-45db-a5b7-034623ef1fa3](https://github.com/user-attachments/assets/b9293257-8596-4e88-8acb-c02d9db0e777)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![433054500-200239d9-4053-4cae-b31b-5b9b3e31b294](https://github.com/user-attachments/assets/68c27e4b-ba0b-4328-9541-9740ce748fa9)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![433054504-97f64eaf-977a-42c4-8b44-cf9b42ff3e0f](https://github.com/user-attachments/assets/8efe37d7-69d0-47bd-8a79-f46a46195e08)


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
![433053550-00c3b103-54f2-422d-ac92-27a0c1dce159](https://github.com/user-attachments/assets/2f7b05ba-5b37-489e-8509-5fdfa66a5adf)

 
ls file1
## OUTPUT
![433053541-b005841a-7afc-4a2c-84d8-2ada90dd7304](https://github.com/user-attachments/assets/517fff88-b384-4cb7-8c0d-4613071fa969)


echo $?
## OUTPUT
![433053529-8e020e6e-e8cb-439f-a2ea-398c45808a17](https://github.com/user-attachments/assets/579e11db-5d0c-47f8-8ef8-a05690d0eee6) 


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![433053529-8e020e6e-e8cb-439f-a2ea-398c45808a17](https://github.com/user-attachments/assets/8b79eb31-f2fa-40d5-9ff7-095ae72f7571)

 
abcd
 
echo $?
 ## OUTPUT
![433053526-3c6037d4-2263-4cd5-8709-aea32077cd23](https://github.com/user-attachments/assets/f0b9d567-cd36-4822-9bcc-1cff2451d4cf)


 
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
##OUTPUT

![433053524-7a005138-4dea-4646-991c-1948da0339bd](https://github.com/user-attachments/assets/bbe475de-a700-472e-b75c-7f712e5b3bbf)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![433053520-a17ed75f-5adc-4f71-9dae-bf2afae9cd32](https://github.com/user-attachments/assets/9a7af687-87ed-4f4e-b57e-6edebbe11801)


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

![433053501-b114db17-ce64-4837-ab59-6f39f5adaa07](https://github.com/user-attachments/assets/c20f79ce-72f4-4d0d-bbb0-4de430c142a8)


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

![433053484-87197e4d-a912-4f3a-a424-78c786f5ef11](https://github.com/user-attachments/assets/4e83b672-a227-4004-9cc4-9325599f90a4)


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
##OUTPUT
![433053475-0fcfc9d5-e6a4-44fe-a62f-b45ec5fd69f5](https://github.com/user-attachments/assets/7add73d2-ac23-4cd9-b281-58bebee0f55d)


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
##OUTPUT
![Uploading 433053465-9fa176e5-b82e-4bbc-a2ce-33388bc23326.png…]()



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
![433053446-67d23544-cd3f-4c5c-b9bc-048b4e7db9d8](https://github.com/user-attachments/assets/79ee2aa7-3885-4af4-a606-9fc209ef42ad)


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
![433053329-25ea03fd-adb2-41b6-aa26-3dad24d33bf5](https://github.com/user-attachments/assets/21f84935-0138-4b5f-a4e8-1a786376b50a)



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
![433053168-0d924b02-cdc9-4f35-9843-d33877e4ca93](https://github.com/user-attachments/assets/37ddbbd5-6ef0-4a4f-bb96-4215ca5300b0)


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
![433053145-69164e28-752e-42bc-8a52-c7e811c51b35](https://github.com/user-attachments/assets/a53dbd5c-1e25-4593-a0e9-52e3074ba2d7)


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
![433053140-d79599c8-1582-4879-ae85-a2876e060388](https://github.com/user-attachments/assets/2fac6b5e-dfec-4efe-8e17-1fcf8da795c9)



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
 ![433053133-d575a381-471a-4198-a53c-bc82d54ec158](https://github.com/user-attachments/assets/a8e82d60-710a-4a96-91fc-dca1ae160502)

$ ./fornested1.sh 
 ## OUTPUT

 
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
![433053115-15ad31aa-f478-46db-967f-ea40969e9140](https://github.com/user-attachments/assets/4e1d6c60-fe62-493f-b16c-8c49cb4d6dce)


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
![433053107-33901b5e-fc5b-4556-8705-334d9a141212](https://github.com/user-attachments/assets/6c89b8a0-6bd6-47c8-8ccb-249e8782c49e)

 
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

![433053102-77d7119e-a08b-4e3b-a87b-37ed1d2a2a8d](https://github.com/user-attachments/assets/fb972a7f-e96a-4307-a0b9-9b14087eb0a4)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![433053097-fdfa0c68-b184-4cbc-8dfa-5001892b8000](https://github.com/user-attachments/assets/bb5fa5c3-93f6-49f0-b28a-0af9866f98ef)


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
 ./funcex.sh 
 ![433053088-35259df3-f9f8-447c-bf6f-79c9c91a41fb](https://github.com/user-attachments/assets/46f89ddc-c1cb-4598-8af9-a3ad6a4c3d0c)

 
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
$ ./argshift.sh 1 2 3
 ![433053082-7330bd8e-343e-4f8c-a7fe-c61e351e17d9](https://github.com/user-attachments/assets/000b55c5-9ca5-47ae-b819-5c793ff03230)

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

![433053034-d49a181b-1433-4598-87fd-19a729efad1d](https://github.com/user-attachments/assets/19112414-a51e-4e98-8696-4e8268e9d78a)

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
![433053027-b3c04c87-a44c-4772-8eb0-979dd58e0c4c](https://github.com/user-attachments/assets/cb147046-34a6-48e8-99c9-aa15ca6785d5)


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
![433053018-69077483-bbe4-4ecb-9b9b-369e8647a7ed](https://github.com/user-attachments/assets/472cb066-604d-4e2d-805f-4f108604cc90)
 
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
![433053001-935772c7-91a1-440c-a0a2-0b8c12cd9b37](https://github.com/user-attachments/assets/522ea15c-4b08-49cf-8f93-7c42fe6367f5)


# RESULT:
The Commands are executed successfully.
