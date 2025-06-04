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

![433053280-6fccd523-1904-4548-b48c-b634a6760137](https://github.com/user-attachments/assets/61cb86e7-1de8-4a77-836f-28e9f721446d)


cat < file2
## OUTPUT
![433053308-5e15f943-716c-4d13-8736-dd26cd96e5c4](https://github.com/user-attachments/assets/2da4c987-aaf4-41c1-906f-0f147a3ee9ee)


# Comparing Files
cmp file1 file2
## OUTPUT

![433053671-3c00b5bd-6bf1-474e-96c2-e136feb99ced](https://github.com/user-attachments/assets/fa9cec5b-09d6-4895-a3a3-7f9fa6a3e4cc)


 
comm file1 file2
 ## OUTPUT
 
 ![433053709-b1cb74f1-7090-425e-8d28-4e8d23fb7bee](https://github.com/user-attachments/assets/0be680ec-a7fe-4d61-ae74-1c4f47f1b2e5)


 
diff file1 file2
## OUTPUT
![433053730-725a14d5-e419-4221-bfa2-97f2580ddd07](https://github.com/user-attachments/assets/87d212e9-3c87-4a78-8832-f344af1c8761)


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

![433054006-8ed6ef0a-beba-4473-8df0-8d1687a2fe43](https://github.com/user-attachments/assets/a3cb0aba-8b34-4174-a86c-89da961e6933)



cut -d "|" -f 1 file22
## OUTPUT
![433054087-cd1005ad-c27e-4fbd-ac2e-54af177ee6b6](https://github.com/user-attachments/assets/3cd37e16-b566-4061-81d7-5da5f227b257)



cut -d "|" -f 2 file22
## OUTPUT
![433054113-4a68ab21-b372-42f2-bd6a-d176014baea9](https://github.com/user-attachments/assets/ba23214d-93da-4329-92b5-a01328cb5095)


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

![433054376-17ceda92-2d8a-4bf0-90a4-d7596be63ed4](https://github.com/user-attachments/assets/2d8c5cac-0295-4a24-9c46-9ce9e6c5d238)


grep hello newfile 
## OUTPUT

![433054409-d3c26ea6-3a5c-4cd4-ae93-42c5e80bc733](https://github.com/user-attachments/assets/08d7f4d3-22f7-4617-9e3d-7607cb0e331a)



grep -v hello newfile 
## OUTPUT

![433054437-e8df394a-05d0-4656-91fd-edc5d244d047](https://github.com/user-attachments/assets/923d5a2a-ad89-4a56-b6ca-b00147ae7e58)


cat newfile | grep -i "hello"
## OUTPUT

![433054472-cc868b4c-3718-4d99-b743-76e442a0b066](https://github.com/user-attachments/assets/9dd25b79-965d-4a86-a1d6-7dc459cc784d)



cat newfile | grep -i -c "hello"
## OUTPUT




grep -R ubuntu /etc
## OUTPUT
![433054645-0546c10e-5a52-4333-971a-d8e04730fd56](https://github.com/user-attachments/assets/8ff47514-f6a0-441a-9370-7547f742ed7f)



grep -w -n world newfile   
## OUTPUT
![433054704-8dc7e9f0-17fc-4d61-b93a-58a0d6e819ac](https://github.com/user-attachments/assets/040f3735-330a-46a3-bfb7-a9a47760df80)


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

![433054800-feb84853-5607-4c01-b959-42f69bdefa06](https://github.com/user-attachments/assets/53054dbe-676f-4ffd-92ca-235d521c6a0d)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![433054842-731431c5-079c-4ccf-8db4-021ca6089613](https://github.com/user-attachments/assets/d5982c6c-9269-4a80-b41d-952d0123c726)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![433054864-12d44307-7b36-4ace-af07-9072125006b0](https://github.com/user-attachments/assets/a4e91f55-09a5-422d-9b7f-9e6845749462)



egrep '(^hello)' newfile 
## OUTPUT

![433054885-b5d7ada9-b952-4770-a459-bb304bec478e](https://github.com/user-attachments/assets/83b4a680-cbca-4bd0-9543-b68618fe43e2)


egrep '(world$)' newfile 
## OUTPUT

![433054915-41eed109-ea90-40a3-a999-bc0c04c010bd](https://github.com/user-attachments/assets/b6f7da62-1325-4190-901c-68e3a44f5a24)


egrep '(World$)' newfile 
## OUTPUT
![433054943-57ffadc5-7e18-429e-ba6e-e12120aa1c76](https://github.com/user-attachments/assets/fa8534ad-a787-47db-b4e1-a199d9b7200b)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![433054974-496d2ed3-92b4-45d0-a55a-78bb1d514b38](https://github.com/user-attachments/assets/e3a96c08-e52b-4572-86d3-eaa202a368cd)


egrep '[1-9]' newfile 
## OUTPUT
![433054997-5ce956c9-6405-44f8-9f92-26c7cbc398f2](https://github.com/user-attachments/assets/416896c5-6137-4628-82e4-38781ce098dc)



egrep 'Linux.*world' newfile 
## OUTPUT
![433055018-a6933d1f-57f4-465b-80ad-e62090dfbd61](https://github.com/user-attachments/assets/a1a44282-04f8-47bc-a4c4-783f91cb7775)


egrep 'Linux.*World' newfile 
## OUTPUT

![433055055-83c2e168-7f8a-438a-aa0d-86e7ec60108d](https://github.com/user-attachments/assets/6b6ac47d-ef35-45fb-a7a6-3de49a9f672c)

egrep l{2} newfile
## OUTPUT

![433055083-7af0fc66-1e70-439e-939d-7e084130f16a](https://github.com/user-attachments/assets/eab0df42-726c-4ee8-aad6-1bf326baa420)


egrep 's{1,2}' newfile
## OUTPUT 

![433055124-377117ef-9e97-4e60-854d-45996cd2847f](https://github.com/user-attachments/assets/e4be4a8c-39d6-4823-81dc-ec117b06b362)

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

![433057185-c2ce5a93-5668-406c-a9c1-84bf3754db39](https://github.com/user-attachments/assets/6026e5a2-9cf5-4f1e-8770-455b97af8b95)


sed -n -e '$p' file23
## OUTPUT
![433057223-8364bc33-4a9f-4159-ad02-af8b07cfa6d3](https://github.com/user-attachments/assets/65a07dc7-7e32-4312-a092-249e9a589a1d)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![433057295-9228794d-8a6e-4cff-be5f-cf1039db1ed8](https://github.com/user-attachments/assets/26628422-48a9-4318-ac3f-86d57322e134)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![433057368-ca777e2e-1a54-4005-b7b3-bd7821535088](https://github.com/user-attachments/assets/159d7aa4-00b3-4fd5-8859-ca560b508daa)




sed  '/tom/s/5000/6000/' file23
## OUTPUT
![433057427-ce747184-bfa9-43b1-afa6-f78bfd1e8abb](https://github.com/user-attachments/assets/311ebe12-437a-468d-87c0-f4f2ad03dc2d)



sed -n -e '1,5p' file23
## OUTPUT

![433057498-ab460fd6-0660-4086-b2cf-0ddb568f9d7a](https://github.com/user-attachments/assets/05f26895-fecc-46ec-9743-371414166fb0)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![433057557-1060fffe-7270-4177-afd9-35174a759c83](https://github.com/user-attachments/assets/b0c320ad-c36b-4f48-8934-09eda949854a)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![433057627-8e631c64-d22e-4dd4-a5aa-ad7a4b805bc4](https://github.com/user-attachments/assets/a0a776b6-c4a8-4a2a-9faf-36fcc86998d3)


seq 10 
## OUTPUT


![433057671-039b436a-8ce8-43ce-a19a-50529d276d87](https://github.com/user-attachments/assets/0cab3a69-1988-41ef-ac84-b7cd2b5c22eb)

seq 10 | sed -n '4,6p'
## OUTPUT

![433057746-0446a37b-d933-4a62-b80b-0343a6bffb7d](https://github.com/user-attachments/assets/3c6bc7b2-713d-4e97-9929-8f150549cffe)


seq 10 | sed -n '2,~4p'
## OUTPUT

![433057784-966bff2f-6c65-4ddd-b8e8-ee600752b064](https://github.com/user-attachments/assets/e7178556-3c87-479d-b296-462fbc2212aa)


seq 3 | sed '2a hello'
## OUTPUT

![433057861-096a7214-6145-4a00-b974-88af55b560fe](https://github.com/user-attachments/assets/0e9076bb-82ee-4265-8b29-4c27bb29bcf2)


seq 2 | sed '2i hello'
## OUTPUT
![433057911-2cefa889-0a78-4333-ac13-97f748021c3b](https://github.com/user-attachments/assets/1b252fa6-5cb0-4acd-83e5-ebd855b56a8c)


seq 10 | sed '2,9c hello'
## OUTPUT
![433057985-c5562130-1224-4718-9bde-1593cf9f541a](https://github.com/user-attachments/assets/5461073a-61e8-4ae5-ac59-303744b78c1e)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![433058084-1a4b9649-70a5-4415-adbc-3c5f555e746f](https://github.com/user-attachments/assets/70676c92-6598-4d83-8063-bb29625bb83d)


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
![433058369-1c75ce5d-8eb5-450c-8e8e-7dc22a322cc6](https://github.com/user-attachments/assets/b28ec752-baf1-4d45-98d3-7ebc29e14734)


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
![433058493-cfe9c371-e39e-4eaa-baaf-d3b617c9c403](https://github.com/user-attachments/assets/af3ad046-1f1b-4079-b64e-9946909f419f)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![433058549-39621e59-7e7d-4a5f-b2b0-71d0077080e0](https://github.com/user-attachments/assets/f28e9afd-d790-44e3-aaba-8d5e39216f40)

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

![433058624-6e523c66-2a83-4c16-a19c-faeb11b9b11c](https://github.com/user-attachments/assets/3ba3d64c-a3e6-4269-9b90-14d88cf4f923)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![433058658-5637df83-3650-4995-b77b-19762d604b2b](https://github.com/user-attachments/assets/c747a341-5400-43f3-9fde-5b2a76a555f2)



#Backup commands
tar -cvf backup.tar *
## OUTPUT

![433058714-af83ce0c-e18b-4be3-8416-8bbdee59d907](https://github.com/user-attachments/assets/ba86f53d-22da-49e4-8966-c97cd2353907)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![433058866-4f102ba9-53e9-4a0e-9ebb-0c24413fc87d](https://github.com/user-attachments/assets/37c71627-0cd8-4d92-9564-a87bcea4ba41)

tar -xvf backup.tar

## OUTPUT
![433058903-98ea7d57-4da9-4d24-a68c-013f91e55229](https://github.com/user-attachments/assets/ba8e7f74-33d8-456a-8cc9-d787f9c191bd)

gzip backup.tar

ls .gz
## OUTPUT
 ![433058983-e54af9c7-1ac4-4bed-a203-c6b780523329](https://github.com/user-attachments/assets/106bfc3b-1368-435c-a76e-f83b26cb9ba4)

gunzip backup.tar.gz
## OUTPUT

 ![433059036-079e2bbb-e95b-4761-bd61-789f1a3dd55f](https://github.com/user-attachments/assets/93015354-0b49-447d-9692-b024f3f786f8)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![433067988-e4af163e-b80a-40fc-bcf1-fa93109286af](https://github.com/user-attachments/assets/84953d19-b787-4d04-a8c3-a19a085ae3f5)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![433068052-14ac7075-3b09-4e91-add5-3456bb13fc66](https://github.com/user-attachments/assets/40b450be-bec8-4562-a880-c450939f6729)

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
![433068530-b953a2f3-5513-4a29-9de6-431e1489c581](https://github.com/user-attachments/assets/debbba16-b7c8-46ce-b86c-cb798492563e)

 
ls file1
## OUTPUT
![433068620-e988dd15-3557-4cdc-9c5a-56afc6dc70ce](https://github.com/user-attachments/assets/97098a87-4f4d-4ae6-97d4-6d0889b3f129)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![433068778-d39c5f62-2db3-4955-84c9-6f954d50ae18](https://github.com/user-attachments/assets/a2b93b30-9816-4608-932c-e62816a84d08)

 
abcd
 
echo $?
 ## OUTPUT
![433069355-a7d96713-1af4-4dcf-ab74-70411b23153f](https://github.com/user-attachments/assets/1155a135-60a3-49cb-85a4-98f5cdd1ac45)


 
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

![433070377-b10f44ee-7d68-4422-af94-d333b28feff2](https://github.com/user-attachments/assets/f2f67ff0-93b1-47de-b835-94dd62c89625)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![433070842-fdc676c2-30b4-4cb5-856a-0f8a4ad6e040](https://github.com/user-attachments/assets/47e8867b-4412-4a6b-990d-fed61cb49dc8)



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
![433070842-fdc676c2-30b4-4cb5-856a-0f8a4ad6e040](https://github.com/user-attachments/assets/f67462c8-405b-4d51-b278-1f6513f455b0)

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

![433071221-005816e4-afad-4995-9435-ee00da64d1fd](https://github.com/user-attachments/assets/a74eca48-c272-4323-8563-44bcbfcfc715)


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
![433071458-4ef6ef44-0b5f-48ac-a075-9ba22be5807d](https://github.com/user-attachments/assets/ceabd713-451c-4573-b607-302b23b6eed7)


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
![433072032-a8130528-2907-4ace-9b34-4a1d6f314c66](https://github.com/user-attachments/assets/60989f38-9c3d-4c3f-a5c2-47e7ee5c2fe7)


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
![433072331-ab09b9e2-280f-4fe8-8351-91a7a6c74c85](https://github.com/user-attachments/assets/a20cb91e-5c82-4cdc-8676-f86a6d5479df)


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
![433072604-fef988a9-668c-4c57-9390-06195de6ec87](https://github.com/user-attachments/assets/a2a1fa20-ab48-45aa-b93a-fed3a3310f34)

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
![433074655-7c63c81f-e699-4029-ad04-5b32b616f33c](https://github.com/user-attachments/assets/692694c1-c08c-46de-9e0b-e46aaf711fe5)

## OUTPUT
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
![433079518-a137aaa7-9661-49c3-b4a6-eb739bd0e876](https://github.com/user-attachments/assets/202b1e17-0d91-4d63-a465-1768cffec29b)


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
![433079648-3072743a-9691-40b4-99ab-5d9189afd9ea](https://github.com/user-attachments/assets/d7de662f-ee3c-4a83-948e-49aa016f275a)

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
![433079699-17775c12-db30-4953-8c3e-1c80482a0cd3](https://github.com/user-attachments/assets/790bdcee-63eb-4fcd-902d-4e5196cb71b0)

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
 ![433079778-88560eb0-ff33-47e4-81bb-88d413240e20](https://github.com/user-attachments/assets/17ad8470-7aa4-4a2a-9d43-d74dd7db87f1)


 
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
 ![433080335-295e60f5-4274-4953-a0df-f0881c625371](https://github.com/user-attachments/assets/213f2fe7-c200-423e-bbda-a0a472eb8c99)

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

![433080473-482c630c-3b9b-42d1-8f95-dcdb431ce8bd](https://github.com/user-attachments/assets/fab37407-b4fe-4e19-8b3e-26d8b2e108e4)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![433080514-a307d5a2-dcea-4379-8a73-4d19df5e70a6](https://github.com/user-attachments/assets/7f6e8618-5d66-4268-bc1c-a47a0af657ba)


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
![433080583-4c206ec8-5809-40bb-8a55-3f72201ffb24](https://github.com/user-attachments/assets/057858f2-961b-401a-a630-c1cd86dc4761)

 
 ./funcex.sh 1 2
![433080610-5355b55a-8615-41eb-b2d6-1291bd114e7a](https://github.com/user-attachments/assets/b0ce8ec1-0b10-494a-b950-b637ce5f2b9d)

 
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


 ![433080680-dd025c0c-d7c2-4882-840e-4070d5e4644b](https://github.com/user-attachments/assets/3e7a27e7-377d-4835-810b-f949d8525cd2)

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

![433080803-e4709e9d-080d-4670-b104-e6616064ce80](https://github.com/user-attachments/assets/096eacd3-7d26-4766-a801-fe72352a9c7c)


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
 ./argshift.sh 1 2 3
 
 ![433080889-77fa2545-28db-4def-a70f-2e4d1dae8f1a](https://github.com/user-attachments/assets/c645bea3-c8a1-48a7-9d78-031c9ba4b021)

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
 ![433081120-209171aa-f009-4f76-b623-c8b364c8f21a](https://github.com/user-attachments/assets/1ea4aea2-8868-4f08-99c7-ec4653eaab8b)

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
![433081217-c67d9c34-9a34-4dba-a619-589ee9ceca73](https://github.com/user-attachments/assets/d7eb5a4f-f597-4d3f-9e9a-ac93356b3fe7)


# RESULT:
The Commands are executed successfully.
