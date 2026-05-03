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
<img width="468" height="157" alt="Screenshot 2026-05-01 112204" src="https://github.com/user-attachments/assets/099b085e-3e6a-4ee8-ac73-98f65efb743c" />

cat < file2
## OUTPUT
<img width="464" height="198" alt="Screenshot 2026-05-01 112325" src="https://github.com/user-attachments/assets/3f6e457c-6848-4e91-839a-fa21a7477882" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="535" height="76" alt="Screenshot 2026-05-01 112413" src="https://github.com/user-attachments/assets/a436de6d-218f-486d-a1db-2c68c40ac2ce" />
 

comm file1 file2
 ## OUTPUT
<img width="635" height="277" alt="Screenshot 2026-05-01 113327" src="https://github.com/user-attachments/assets/a4ddecd5-5209-42d6-bfac-eb417b2b7943" />

 
diff file1 file2
## OUTPUT
<img width="493" height="279" alt="Screenshot 2026-05-01 113356" src="https://github.com/user-attachments/assets/5e37063f-a993-47de-a99e-3cca7a5a818b" />


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
<img width="374" height="102" alt="Screenshot 2026-05-01 113603" src="https://github.com/user-attachments/assets/0d2ac710-f708-4bed-bf1f-709502e13abf" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="383" height="125" alt="Screenshot 2026-05-01 113638" src="https://github.com/user-attachments/assets/55cc37a3-6256-4e33-b690-eef31c1c08da" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="423" height="121" alt="Screenshot 2026-05-01 113709" src="https://github.com/user-attachments/assets/80979441-536e-4193-a755-17c54337e3a9" />


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
<img width="370" height="66" alt="Screenshot 2026-05-01 113921" src="https://github.com/user-attachments/assets/6654440d-1c1e-4f79-b74d-8cb6988240e0" />


grep hello newfile 
## OUTPUT
<img width="366" height="79" alt="Screenshot 2026-05-01 113956" src="https://github.com/user-attachments/assets/adbf4626-b7e0-489b-8982-fa672551d90c" />




grep -v hello newfile 
## OUTPUT
<img width="412" height="78" alt="Screenshot 2026-05-01 114034" src="https://github.com/user-attachments/assets/b24b4bd0-770d-4dee-94f1-d6e01e9020b8" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="368" height="108" alt="Screenshot 2026-05-01 114108" src="https://github.com/user-attachments/assets/e9fc8480-8ba5-4487-b5c1-50383d4f33da" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="432" height="71" alt="Screenshot 2026-05-01 114146" src="https://github.com/user-attachments/assets/21d50780-92bf-4d0e-9095-030e3037ae67" />




grep -R ubuntu /etc
## OUTPUT
<img width="1329" height="550" alt="Screenshot 2026-05-01 114401" src="https://github.com/user-attachments/assets/d730077f-de6e-4fc8-9d07-54294b262824" />



grep -w -n world newfile   
## OUTPUT
<img width="483" height="102" alt="Screenshot 2026-05-01 114454" src="https://github.com/user-attachments/assets/cbfcd1fb-abe3-4257-99aa-cecac2de467b" />



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
<img width="433" height="108" alt="Screenshot 2026-05-01 114628" src="https://github.com/user-attachments/assets/9f92be1d-e4a4-41bc-a527-f09cd526bf9a" />


egrep -w '(H|h)ello' newfile 


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="457" height="103" alt="Screenshot 2026-05-01 114711" src="https://github.com/user-attachments/assets/5ae85a4b-eac5-4b2b-bd30-88fc60d46b86" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="425" height="79" alt="Screenshot 2026-05-01 114745" src="https://github.com/user-attachments/assets/0f3697e6-ff39-4172-9f11-f8bf81046930" />



egrep '(world$)' newfile 
## OUTPUT
<img width="406" height="110" alt="Screenshot 2026-05-01 114821" src="https://github.com/user-attachments/assets/70c4f878-e4f7-4ac9-9af7-0249c8a2b2e7" />


egrep '(World$)' newfile 
## OUTPUT
<img width="449" height="78" alt="Screenshot 2026-05-01 114857" src="https://github.com/user-attachments/assets/a742c14d-d94b-4772-b99e-c43962fb96b1" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="479" height="131" alt="Screenshot 2026-05-01 114944" src="https://github.com/user-attachments/assets/d888b28a-afd6-4978-ba5d-f248c8b2df7a" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="427" height="77" alt="Screenshot 2026-05-01 115019" src="https://github.com/user-attachments/assets/c513b563-dec9-4b6e-96c0-35e3514f3f27" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="453" height="81" alt="Screenshot 2026-05-01 115100" src="https://github.com/user-attachments/assets/089f06a7-c73a-4072-8111-42fd680f428b" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="504" height="78" alt="Screenshot 2026-05-01 115146" src="https://github.com/user-attachments/assets/ab3c1726-8094-409e-80ec-a9360454b30f" />



egrep l{2} newfile
## OUTPUT
<img width="460" height="105" alt="Screenshot 2026-05-01 115214" src="https://github.com/user-attachments/assets/d486d946-a409-46d3-a480-3afd0c10fbf6" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="408" height="129" alt="Screenshot 2026-05-01 115250" src="https://github.com/user-attachments/assets/fb549f7a-6a54-4da9-a3a8-ff1937152c6e" />



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
<img width="515" height="85" alt="Screenshot 2026-05-01 115350" src="https://github.com/user-attachments/assets/92623461-387a-4e75-9fc1-21f66e2bfa78" />


sed -n -e '$p' file23
## OUTPUT
<img width="506" height="79" alt="Screenshot 2026-05-01 115758" src="https://github.com/user-attachments/assets/9b98158e-d661-4f7d-bcf2-39bc20b9b650" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="487" height="251" alt="Screenshot 2026-05-01 115838" src="https://github.com/user-attachments/assets/374474ed-dfe0-483a-b362-d2aaaafa67a8" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="408" height="254" alt="Screenshot 2026-05-01 115913" src="https://github.com/user-attachments/assets/da9de056-cbde-4ef2-aec2-e2ee44b2333a" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="530" height="251" alt="Screenshot 2026-05-01 115949" src="https://github.com/user-attachments/assets/5e9f4585-7c0a-4053-8800-67fdf8867036" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="479" height="176" alt="Screenshot 2026-05-01 120027" src="https://github.com/user-attachments/assets/a41f9f09-1248-44b9-9e7c-357cb37942d7" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="426" height="128" alt="Screenshot 2026-05-01 120105" src="https://github.com/user-attachments/assets/eb7f80b9-65e7-4469-b551-8eca4e59614a" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="484" height="101" alt="Screenshot 2026-05-01 124224" src="https://github.com/user-attachments/assets/cea3e1cd-cd7b-46cd-9326-3b80e1f86194" />



seq 10 
## OUTPUT
<img width="481" height="298" alt="Screenshot 2026-05-01 124251" src="https://github.com/user-attachments/assets/b9b4a97a-3bbe-46e3-9fb2-5fbd5685a4a6" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="395" height="122" alt="Screenshot 2026-05-01 124322" src="https://github.com/user-attachments/assets/873ca190-9caa-41c4-8fc7-e23150bd7388" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="451" height="125" alt="Screenshot 2026-05-01 124359" src="https://github.com/user-attachments/assets/a786c9bf-dcb7-40e5-984f-bcbfbbfd1a42" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="380" height="149" alt="Screenshot 2026-05-01 124426" src="https://github.com/user-attachments/assets/e45e6288-14fd-4876-91fb-f7db8266d7d7" />

seq 2 | sed '2i hello'
## OUTPUT
<img width="455" height="125" alt="Screenshot 2026-05-01 124457" src="https://github.com/user-attachments/assets/0b6c7c08-6f17-449f-8e77-98eb558f1ac2" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="427" height="130" alt="Screenshot 2026-05-01 124526" src="https://github.com/user-attachments/assets/4b68d626-6250-4af7-8d6d-c81f24da767f" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="411" height="127" alt="Screenshot 2026-05-01 124617" src="https://github.com/user-attachments/assets/c13ff322-316f-41b4-a146-2e9ea1b807a8" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="464" height="127" alt="Screenshot 2026-05-01 124659" src="https://github.com/user-attachments/assets/58a193c3-dc50-4f6e-93aa-de7bc67ed2f6" />



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
<img width="378" height="180" alt="Screenshot 2026-05-01 124741" src="https://github.com/user-attachments/assets/a2a46512-cc66-4cde-af57-80e1f179825c" />



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
<img width="383" height="173" alt="Screenshot 2026-05-01 124824" src="https://github.com/user-attachments/assets/d536498f-0c4f-4fc4-924c-ab1b7ff0ae89" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="597" height="207" alt="Screenshot 2026-05-01 124917" src="https://github.com/user-attachments/assets/282bfa38-232c-409b-883d-ad61b19644f3" />


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
<img width="419" height="130" alt="Screenshot 2026-05-01 125115" src="https://github.com/user-attachments/assets/68316c4e-f3aa-480b-b2cb-73565cdc7384" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="499" height="127" alt="Screenshot 2026-05-01 125213" src="https://github.com/user-attachments/assets/619f3cab-4901-4f85-9f84-8dc5f6260439" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="758" height="545" alt="Screenshot 2026-05-01 125347" src="https://github.com/user-attachments/assets/e682892b-63fe-4b11-9f88-636919630174" />



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1205" height="598" alt="Screenshot 2026-05-01 125608" src="https://github.com/user-attachments/assets/508fd0db-4a23-4584-8b2e-8631466607cf" />



tar -xvf backup.tar
## OUTPUT
<img width="982" height="548" alt="Screenshot 2026-05-01 125709" src="https://github.com/user-attachments/assets/7c6a6f00-6a22-4cf8-94e0-3d8b018d5c0f" />



gzip backup.tar

ls .gz
## OUTPUT
<img width="582" height="79" alt="Screenshot 2026-05-01 125847" src="https://github.com/user-attachments/assets/8e83fe6a-6757-4934-b122-d4cb05745273" />
 


gunzip backup.tar.gz
## OUTPUT
<img width="897" height="280" alt="Screenshot 2026-05-01 130103" src="https://github.com/user-attachments/assets/dc7284e9-f03d-4cf9-b408-dd3ef911bd56" />



# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘;exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="425" height="125" alt="Screenshot 2026-05-01 130601" src="https://github.com/user-attachments/assets/f4d8dda0-3352-47fb-8cad-3c28b09058eb" />


cat < scriptest.sh 
```bash
#!/bin/sh
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
```

cat scriptest.sh 
```bash
#!/bin/sh
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

<img width="547" height="378" alt="Screenshot 2026-05-01 130804" src="https://github.com/user-attachments/assets/b42f1fcd-1117-4aec-ab66-52818f99c56e" />


ls file1
## OUTPUT

<img width="404" height="82" alt="Screenshot 2026-05-01 130829" src="https://github.com/user-attachments/assets/59f74830-8d64-4354-ae0f-85983374639d" />


echo $?
## OUTPUT 

<img width="373" height="80" alt="Screenshot 2026-05-01 130849" src="https://github.com/user-attachments/assets/f6fe8ffe-4230-4082-8806-ecd3773db331" />


./onebash:./one: Permission denied
 
echo $?
## OUTPUT 
 
<img width="525" height="154" alt="Screenshot 2026-05-01 130941" src="https://github.com/user-attachments/assets/7edd932f-afee-452a-9bab-547f28f12874" />


abcd
 
echo $?
 ## OUTPUT

<img width="565" height="155" alt="Screenshot 2026-05-01 131005" src="https://github.com/user-attachments/assets/53e0dfe8-950b-48a8-8ec0-0c04a06ea358" />

 
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
#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
chmod 755 strcomp.sh 
./strcomp.sh 
## OUTPUT

<img width="614" height="107" alt="Screenshot 2026-05-01 131341" src="https://github.com/user-attachments/assets/8e6153d5-daa1-4838-baa9-379708362ae6" />


# check file ownership
cat < psswdperm.sh 
```bash
#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
```

cat psswdperm.sh 
```bash
#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT

<img width="576" height="83" alt="Screenshot 2026-05-01 131713" src="https://github.com/user-attachments/assets/aec79278-bdad-48e2-bdaa-86e5e55b3fcb" />


# check if with file location
cat>ifnested.sh 
```bash
#!/bin/bash
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
cat ifnested.sh 
```bash
#!/bin/bash
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

<img width="486" height="81" alt="Screenshot 2026-05-01 131854" src="https://github.com/user-attachments/assets/f8fd50eb-545d-4e8b-9bd6-4510739b9bbe" />


# using numeric test comparisons
cat > iftest.sh 
```bash
#!/bin/bash
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


cat iftest.sh 
```bash
#!/bin/bash
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

chmod 755 iftest.sh
 
./iftest.sh 
## OUTPUT

<img width="460" height="104" alt="Screenshot 2026-05-01 132011" src="https://github.com/user-attachments/assets/3fcef47a-92f9-4eb2-bd7d-53d029df503e" />


# check if a file
cat > ifnested.sh 
```bash
#!/bin/bash
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

cat ifnested.sh 
```bash
#!/bin/bash
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

<img width="601" height="130" alt="Screenshot 2026-05-01 132123" src="https://github.com/user-attachments/assets/02b08492-ff1e-4eeb-97ec-a2a619296645" />


# looking for a possible value using elif
cat elifcheck.sh 
```bash
#!/bin/bash
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

chmod 755 elifcheck.sh
 
./elifcheck.sh 
## OUTPUT

<img width="397" height="83" alt="Screenshot 2026-05-01 132251" src="https://github.com/user-attachments/assets/9f64a233-69d6-41b9-860f-4bd829c8baea" />


# testing compound comparisons
cat> ifcompound.sh 
```bash
#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
chmod 755 ifcompound.sh
./ifcompound.sh 
## OUTPUT

<img width="486" height="82" alt="Screenshot 2026-05-01 132345" src="https://github.com/user-attachments/assets/1d1b484d-d0c2-4ac7-b115-03cfb89c8603" />


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

<img width="466" height="79" alt="Screenshot 2026-05-01 132437" src="https://github.com/user-attachments/assets/b9a8b0a3-5364-4a9c-919f-be132ca2c9b6" />


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
chmod 755 whiletest.sh
 
./whiletest.sh
 ## OUTPUT
<img width="401" height="302" alt="Screenshot 2026-05-01 132544" src="https://github.com/user-attachments/assets/eadf0976-9418-4b59-8383-1b3becbc93ca" />

 
cat untiltest.sh 
```bash
#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
$ ./untiltest.sh
 ## OUTPUT

<img width="417" height="149" alt="Screenshot 2026-05-01 132647" src="https://github.com/user-attachments/assets/f7da1d87-9bbb-482a-89d1-b5754ac0f3e9" />


cat forin1.sh 
```bash
#!/bin/bash
#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
$ ./forin1.sh
## OUTPUT

<img width="403" height="205" alt="Screenshot 2026-05-01 132816" src="https://github.com/user-attachments/assets/b478dfdf-13d4-42ae-8359-fd3e5cfd7c45" />

 
cat forin2.sh 
```bash
#!/bin/bash
# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
## OUTPUT
<img width="504" height="127" alt="Screenshot 2026-05-01 132943" src="https://github.com/user-attachments/assets/d4032236-3f4c-4734-a82a-635686b4d7b9" />


cat forin3.sh 
```bash
#!/bin/bash
# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ chmod 755 forin3.sh
$ ./forin3.sh 
## OUTPUT
<img width="411" height="203" alt="Screenshot 2026-05-01 133049" src="https://github.com/user-attachments/assets/500c34c3-7d45-4470-a9e4-bb4325f49265" />


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
$ ./forin1.sh
## OUTPUT

<img width="568" height="209" alt="Screenshot 2026-05-01 133151" src="https://github.com/user-attachments/assets/2f03d97e-0064-4b35-af8e-195764096629" />


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

$ cat > cities
```
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam
```
./forinfile.sh

cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
```
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

<img width="393" height="177" alt="Screenshot 2026-05-01 133646" src="https://github.com/user-attachments/assets/ab50fd72-24a1-4420-b521-54e739891c03" />


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

<img width="373" height="176" alt="Screenshot 2026-05-01 133933" src="https://github.com/user-attachments/assets/e000b7ac-5c53-4108-b9a4-1f13e5ece7ae" />


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

<img width="403" height="350" alt="Screenshot 2026-05-01 134027" src="https://github.com/user-attachments/assets/0156360c-27f5-4a9c-b149-f5729759b0b6" />


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

<img width="365" height="98" alt="Screenshot 2026-05-01 134201" src="https://github.com/user-attachments/assets/f065350c-8cd4-420c-961e-84603576daf5" />


cat > forcontinue.sh 
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
 
<img width="372" height="151" alt="Screenshot 2026-05-01 134251" src="https://github.com/user-attachments/assets/488697df-cab9-4b6f-9fff-bf9920b51a31" />


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

<img width="553" height="100" alt="Screenshot 2026-05-01 134406" src="https://github.com/user-attachments/assets/5c300185-af7f-4c89-9e08-42ee3004013b" />


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

<img width="635" height="106" alt="Screenshot 2026-05-01 134601" src="https://github.com/user-attachments/assets/9c71dbe9-d1d9-4a7a-a891-c3d5b0fdb102" />

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
$ chmod 755 funcex.sh
$ ./funcex.sh 

## OUTPUT
 
<img width="488" height="73" alt="Screenshot 2026-05-01 134654" src="https://github.com/user-attachments/assets/824f21b1-f90b-4ec1-86fd-f09655dc9a12" />

 
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

<img width="364" height="122" alt="Screenshot 2026-05-01 134806" src="https://github.com/user-attachments/assets/3fbddec5-7752-49a5-8263-d270bf390da2" />

 
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
$ chmod 777 argshift1.sh

$ ./argshift1.sh 1 2 3
## OUTPUT

<img width="344" height="126" alt="Screenshot 2026-05-01 134857" src="https://github.com/user-attachments/assets/a0f52fb4-023f-4c9d-930e-d3926d60c858" />

 
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

./argshift.sh 1 2 3
## OUTPUT
 
 <img width="344" height="126" alt="Screenshot 2026-05-01 134857" src="https://github.com/user-attachments/assets/77c4ac66-10ce-40a7-a5d4-5517abe467c7" />

 
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

<img width="400" height="371" alt="Screenshot 2026-05-01 135143" src="https://github.com/user-attachments/assets/6a631bfb-781e-4197-9c11-fd74740c306e" />

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
$chmod 755 palindrome.sh

$./palindrome.sh
## OUTPUT 

<img width="502" height="123" alt="Screenshot 2026-05-01 135246" src="https://github.com/user-attachments/assets/6297e8fa-c902-4e89-a16f-4b01bbdf0881" />

# RESULT:
The Commands are executed successfully.
