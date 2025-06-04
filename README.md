# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting
## Name: KARTHIKEYAN S
## Reg no: 212224230116
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


![309798830-645747f6-840a-4fb5-9bb8-3d37985808e1](https://github.com/user-attachments/assets/805c8d04-bd8c-4d3f-a55d-6fa7af4c9637)

cat < file2
## OUTPUT
![309799356-4680c410-0f1a-417d-9f0d-05e417dff105](https://github.com/user-attachments/assets/efaf5701-0c28-430a-8241-d473d3cfac57)


# Comparing Files
cmp file1 file2
## OUTPUT
![309799683-b72ea53a-f252-420f-b008-c1db50733c87](https://github.com/user-attachments/assets/ffdc4cf8-f945-4c1a-951e-3d8cad6d58fc)

 
comm file1 file2
 ## OUTPUT

 ![309800849-9d8206de-18fe-42e7-98c7-f58a03d1e027](https://github.com/user-attachments/assets/eca07d57-39e4-4575-89a9-42a15d9084dc)

diff file1 file2
## OUTPUT
![309800157-9db3fd92-ee1d-45f1-81b7-2421566f2f4a](https://github.com/user-attachments/assets/c1e0ccd3-c4ec-42e2-8304-921491512d1a)


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

![309801929-b05fb00f-680e-478f-bf30-40e73ed3f8fc](https://github.com/user-attachments/assets/1eae7db2-d439-4dfb-b26f-f4a0cf7b67f3)



cut -d "|" -f 1 file22
## OUTPUT
![309802390-9b1db5ba-2294-4c27-93e3-04529c484132](https://github.com/user-attachments/assets/76ecca5d-9aba-49f3-9204-a25bfa069fc8)



cut -d "|" -f 2 file22
## OUTPUT

![309802553-ac5c3093-ce26-4a44-8342-2861d83fe00c](https://github.com/user-attachments/assets/87436b8a-3a1b-42c1-83e8-17ca7f61693c)

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
![309804197-c9dcc002-ec57-4d2a-ac12-b2118670b418](https://github.com/user-attachments/assets/36b9231e-ed9e-4206-8ddf-aa23427025c8)



grep hello newfile 
## OUTPUT

![309803542-1ba59f65-d89a-443c-b63e-658844690510](https://github.com/user-attachments/assets/b69ff7fd-d8d3-4cf6-9a32-0de13ec15914)



grep -v hello newfile 
## OUTPUT

![309804420-7898aa37-f171-4dd3-b9bf-4821a7c66366](https://github.com/user-attachments/assets/cbf31edd-ec02-4ea2-a59a-c696705110e1)


cat newfile | grep -i "hello"
## OUTPUT
![309804644-b34be529-da32-4875-ada4-5403c4b2b219](https://github.com/user-attachments/assets/dbf28866-04f9-41ce-b36b-6c88cd56eded)




cat newfile | grep -i -c "hello"
## OUTPUT
![309804896-b68bbe48-76d8-4261-aea9-5b3525862b73](https://github.com/user-attachments/assets/2b7d0f2c-f74d-4fcb-b74e-d22c2fa5ab53)




grep -R ubuntu /etc
## OUTPUT

![309805946-c7641628-681a-431e-a85d-f9606f4a5cf5](https://github.com/user-attachments/assets/48a059e8-8707-4824-b7f3-f97513496c99)


grep -w -n world newfile   
## OUTPUT
![309806230-ab89cc80-61df-49c7-b155-4a5e5172bb58](https://github.com/user-attachments/assets/2e82b679-41a4-4394-90c9-0a033eddfd56)


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

![309807165-3fb6eac9-fb4a-4396-9418-c277da0ac7af](https://github.com/user-attachments/assets/e97ac60b-c3b4-4013-97a7-8de662e22750)


egrep -w '(H|h)ello' newfile 
## OUTPUT
![309807392-15faa397-b760-4e38-88c5-46df8d1bdb60](https://github.com/user-attachments/assets/99c9953c-a60f-4cf7-a0a3-f740e014a569)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![309807587-cb5df577-6ca4-4fb2-a5b2-a1bbfc9342ff](https://github.com/user-attachments/assets/350d46bd-cd7b-4b94-9605-8eb94a9d234e)


egrep '(^hello)' newfile 
## OUTPUT
![309807775-84e6db99-923d-4dcb-9d2f-f759f1d23029](https://github.com/user-attachments/assets/52215c1e-76d4-4fbf-a904-e62b5011dfd9)



egrep '(world$)' newfile 
## OUTPUT

![309807775-84e6db99-923d-4dcb-9d2f-f759f1d23029](https://github.com/user-attachments/assets/a6482900-a2f4-4e2e-a3a6-f87c866a96e0)


egrep '(World$)' newfile 
## OUTPUT
![309811412-73eb50dd-a4e7-4231-93fd-3043957f5bb6](https://github.com/user-attachments/assets/c7ae1c5f-c2ef-4d96-82eb-7acb5493a444)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![309811661-10d9f5b0-41c6-4871-8acb-7c1bbfbefaaa](https://github.com/user-attachments/assets/1f866059-1937-418f-a23c-6e0063e26c01)



egrep '[1-9]' newfile 
## OUTPUT

![309813236-56fd1f75-45fe-46f6-8ed2-f25c8c712aec](https://github.com/user-attachments/assets/1bc3998a-3cdc-4c9c-8816-d19f9757b917)


egrep 'Linux.*world' newfile 
## OUTPUT
![309813430-7d6419cf-634f-4106-9a64-86fb2f8098c3](https://github.com/user-attachments/assets/6444a0f6-d10f-4276-9deb-94336c29b5cd)


egrep 'Linux.*World' newfile 
## OUTPUT
![309813792-1128e562-d671-4878-a83c-49a308d4f983](https://github.com/user-attachments/assets/0875b7d6-4492-44e9-a5fe-a5dd5ad3f74a)


egrep l{2} newfile
## OUTPUT
![309814070-da8d070f-5f44-421c-b63e-b08b08021b2d](https://github.com/user-attachments/assets/1627b1cc-2eda-4f70-b8cd-9e73b7c0a621)



egrep 's{1,2}' newfile
## OUTPUT 
![309814327-c79a5769-68c8-4842-87e9-d9799398d1dc](https://github.com/user-attachments/assets/403c2114-4c6b-404a-b46a-d3cfc64e9344)


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

![309814693-d023edb3-6837-4065-98e9-08bb8b5d4360](https://github.com/user-attachments/assets/7f78025e-b48c-4a0f-8249-8a606283ebbe)


sed -n -e '$p' file23
## OUTPUT

![309815013-4c0977d9-7438-4ace-a89a-e0536e3c96b0](https://github.com/user-attachments/assets/33c2af76-8621-4156-ab29-db6833565495)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![309815343-03ea1332-8ae5-4e5b-9f27-5f150319a13b](https://github.com/user-attachments/assets/27bc43d7-d5af-4ac4-8207-a52bee9056e9)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![309815611-54e0938a-b87e-4a52-a6d8-1d33b644ef58](https://github.com/user-attachments/assets/0829fd04-9924-4f95-8a70-0f9d22804af3)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![309815956-f4539868-4ccb-480e-a828-de27371cc413](https://github.com/user-attachments/assets/f6ddc3ba-8701-4ec8-aafa-38c32135e742)


sed -n -e '1,5p' file23
## OUTPUT

![309816318-61c2937f-7b06-4bae-828a-7e00818b5287](https://github.com/user-attachments/assets/a8814c32-8130-4248-a344-0399e4a54659)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![309819642-07aa75ef-5b1e-4d5b-bfe5-7d36cb65c8d7](https://github.com/user-attachments/assets/88769d69-74e1-4aed-b2df-319890bb6a15)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![309819759-b3664d94-dc31-448c-88b1-e74cd741c96b](https://github.com/user-attachments/assets/ef6c6e87-8c73-4564-a28d-9525ad08ff17)


seq 10 
## OUTPUT

![309819968-b51046e0-51df-4a04-97a3-9aff3b3929fd](https://github.com/user-attachments/assets/760ac0f5-5267-46be-a2f5-497a9700d912)


seq 10 | sed -n '4,6p'
## OUTPUT

![309820170-4ed9f3b2-3d9a-4859-a477-9c4d47247f26](https://github.com/user-attachments/assets/a461300f-7204-4f6e-8128-a2332264abb8)


seq 10 | sed -n '2,~4p'
## OUTPUT

![309820615-a910466b-be1c-4335-8842-201a475247b6](https://github.com/user-attachments/assets/3fa0c03e-d1c6-470d-942f-bc764b69edd1)


seq 3 | sed '2a hello'
## OUTPUT

![309820771-40491877-b232-4596-96a2-c3d9955510e8](https://github.com/user-attachments/assets/d0b1fc11-9589-4cc9-9be0-3c365bda0009)


seq 2 | sed '2i hello'
## OUTPUT
![309821238-c0cd675e-bff0-4f16-a406-081556b997ad](https://github.com/user-attachments/assets/a77fca1c-4678-4acd-8fdc-9cda70da3c3e)



seq 10 | sed '2,9c hello'
## OUTPUT

![309821431-0867c436-fe08-4955-b19f-d73264f8008b](https://github.com/user-attachments/assets/c3602354-0982-4874-aec4-0e1ae759c5d5)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![309821572-97a3d875-4b77-48e6-bba7-a65eedd77df3](https://github.com/user-attachments/assets/cc37a9f1-d1a7-4ab6-bbfd-b5cad1dbe7f7)


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
![309822352-ef7e2f21-aca3-4acd-818a-4f55a6cc180b](https://github.com/user-attachments/assets/67287f55-7422-443c-bcaf-0c961b6ab1a5)


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

![309823420-1f2963c8-35ed-4d50-9053-02ce2a88be06](https://github.com/user-attachments/assets/b2e25ccf-3d4b-4951-b876-25da60b99661)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![309823860-dbf6ba03-73d0-4af8-8dc3-0d50d2d6afb4](https://github.com/user-attachments/assets/a456074f-f0af-4c2b-b406-f26e742023e7)

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

![309824719-0729a6c7-8b70-4a6e-93dd-369f6a699821](https://github.com/user-attachments/assets/0ec26043-b6cc-45e1-b20f-a8429e9b79c4)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![309824984-36ecee6f-5496-4b22-909a-5fe77534e6dc](https://github.com/user-attachments/assets/a9ac68f7-67ef-450b-ab55-970bdb704da6)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![309825316-81b64612-f73a-4d36-8b08-a1615ab5e326](https://github.com/user-attachments/assets/fbca18d9-de41-40a3-b913-84b09fe4f803)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![309825519-eb10b39d-0ce2-4e71-ab67-37fc7cc9d18b](https://github.com/user-attachments/assets/98d2ad2b-823e-4e8a-ae4a-bfb802688a6c)


tar -xvf backup.tar
## OUTPUT
![309826053-1b4ddf40-3c5d-45e7-ae2b-914819b4c2ec](https://github.com/user-attachments/assets/bb903053-6528-46d6-b369-d8e8be2261eb)

gzip backup.tar

ls .gz
## OUTPUT
 ![309827418-f9334fa8-a252-415c-b056-c1f9b5d80b38](https://github.com/user-attachments/assets/57fc2b6d-5378-4c44-8ca8-620bd8c46a94)

gunzip backup.tar.gz
## OUTPUT
![309828162-5f0b0094-2c2c-40f3-884f-0c0dcecc24f1](https://github.com/user-attachments/assets/62a481a7-3965-4bd2-96b6-2397123787a9)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![309830670-c7f6eac0-d1a0-4703-9a07-2d631edd84d7](https://github.com/user-attachments/assets/4b69c7f1-32ff-410f-9489-14c616a1e3b9)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![309831247-18cbf086-541c-4bb1-92ab-c814bdf8c142](https://github.com/user-attachments/assets/03978052-9e7c-4c58-b2e8-d5cd9bd16285)

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
![309832793-888cca6e-adb3-4897-99a7-fd743ee6f1bd](https://github.com/user-attachments/assets/71ab55d4-e9ae-45d5-8872-cf5dec5a514c)

 
ls file1
## OUTPUT
![309833097-8aa7a308-1319-4bfe-b9c2-7929272e63cc](https://github.com/user-attachments/assets/a01fddda-ed24-4469-b9e4-b5052070ca36)


echo $?
## OUTPUT 
![309833203-f0d7cbbc-d1eb-42b7-830b-91c7bc5797f4](https://github.com/user-attachments/assets/f5968405-687c-40b7-90e3-3ed9dfebde17)


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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
![309833825-35a3a9c0-5224-4e0f-bae9-6c603032ec8e](https://github.com/user-attachments/assets/43728319-60e4-4b61-afd6-93df9aadab67)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![309834353-a22b99b0-1191-4cd0-a055-a3206264951b](https://github.com/user-attachments/assets/fc2e3e97-ce2b-4ea7-b480-1efc39051ede)


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
![309835594-f984545d-33bc-4b82-833f-e994e20beb27](https://github.com/user-attachments/assets/24d1cf1c-a546-4766-a815-a93a24b6a835)

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

![309836204-d95b622a-155f-4e82-a895-818b862dbca1](https://github.com/user-attachments/assets/c3043d6c-bfc0-4ada-b810-7cdb49922846)


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
![309836560-031d4ce7-6bf5-4cf0-9ef6-3c6fad1b8752](https://github.com/user-attachments/assets/5040016d-52d4-4265-ac71-98f747c52c72)

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
![309837253-b67da7ca-c91d-4a9f-8d63-c24b01a28434](https://github.com/user-attachments/assets/28606969-4348-429f-b39f-5d4b13f528ef)

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
![309837620-a955d321-158d-46a5-a932-dbe21449c991](https://github.com/user-attachments/assets/79a4e290-db98-4d12-a525-4b01535b93e8)


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
![309839617-24882ffa-4666-48a8-80b0-92c170da5e60](https://github.com/user-attachments/assets/e71c399a-4aad-4494-bda2-fa2626a11068)

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
![309840177-fd8b7441-e413-4c34-b35e-72d6b8e953bd](https://github.com/user-attachments/assets/129ea256-3541-4269-9f6e-21e96c59caf2)

 
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
![309840585-e4f9b365-56ff-4898-b0fd-44843212470a](https://github.com/user-attachments/assets/c9ab7d56-5c3c-4dda-84a2-4035db7a1827)

 
 
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
 
 ![309840951-22431f68-6b65-49ec-9287-eeb6d31792a4](https://github.com/user-attachments/assets/b4826e6d-4797-4147-831c-7a9be680a66d)

 
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
 ![309841701-8766aba0-572e-4a9b-bd39-03c7e64820b1](https://github.com/user-attachments/assets/d39195db-ec9f-4811-a108-e164d77be705)

 
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
## OUTPUT
![309842258-169751ae-053b-424e-b0ab-63ef3308d633](https://github.com/user-attachments/assets/d5e022df-bab9-4d0f-a3ea-8e495d855750)

 
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
## OUTPUT
![309842703-20318e60-4a59-472f-ac43-2f3fb6dcd9b9](https://github.com/user-attachments/assets/87eb809d-fc06-4fd1-869e-0060b759e9d7)

 
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
![309843870-1ee1082b-0af5-42d2-8088-78ba28ca6c20](https://github.com/user-attachments/assets/8e64a9be-7c12-487d-9773-af65e4532403)


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
![309844476-18486ab6-4411-45e3-8f9f-fa86c28172a5](https://github.com/user-attachments/assets/76bb2691-36e7-4fd8-9533-f1c356955682)


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
![309844741-841f1a13-e515-4529-b171-cd063a871600](https://github.com/user-attachments/assets/7a8042c2-f3b7-483d-a054-fa5f944ec21d)

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

 ![309845143-1bdc895e-f05e-4992-9c84-b482adc312d0](https://github.com/user-attachments/assets/7d5e7e4c-f20f-4498-8fa9-689bce33473f)

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
![309847528-b8396871-2ea9-4236-8a0b-f7ca315c2d98](https://github.com/user-attachments/assets/950e28f5-1d5d-4fb3-914a-7ac16ef7e5dd)

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
 ~$ chmod 755 exread.sh
 ~$ ./exread.sh
 Enter your name: saranya
 Hello saranya, welcome to my program.

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
![312459255-d669903b-8d7b-4868-a9aa-77537b5ca65b](https://github.com/user-attachments/assets/316af4e7-62ec-4416-97cd-39b49f9ccb87)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![309851670-f8502838-935e-4fda-9fe1-502e60e42c68](https://github.com/user-attachments/assets/073e0bea-9db0-4c3a-8661-0219ab3778d0)



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

 ./funcex.sh 

 
 ./funcex.sh 1 2
## OUTPUT
 ![309852244-62cd062e-c179-4e5a-9ab8-9a83f6b78032](https://github.com/user-attachments/assets/6d16c738-2536-4ebb-ac7a-a22544bd513d)

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

 ![309853113-e82552ac-1446-4b63-91a2-fe9947fa3ca3](https://github.com/user-attachments/assets/d8e2ea70-c9d6-450e-8a63-04652676be2d)

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

![309853667-c104a58c-d3d6-4d6b-930b-d7779001e0ea](https://github.com/user-attachments/assets/64694264-7304-4111-919c-7e22412887db)


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
![309853957-be6b3831-7903-4684-a5ad-4969e49f766a](https://github.com/user-attachments/assets/b2a6bb76-7573-494a-8c03-25e6e1d7e9ab)


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
 ![309854432-6cc7231e-1fe4-4a75-8d76-712cf7246e4a](https://github.com/user-attachments/assets/d62f1cc8-6cbe-43cf-93b2-a3f9a08fad3d)

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
![309855037-9d97b191-3f17-43eb-8883-e773907c2eea](https://github.com/user-attachments/assets/8b4f1a0d-91f5-4a3a-b9b8-6caca36612e5)


# RESULT:
The Commands are executed successfully.
