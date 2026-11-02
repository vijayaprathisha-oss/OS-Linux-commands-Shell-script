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

<img width="270" height="167" alt="image" src="https://github.com/user-attachments/assets/1e8b5ccd-7c74-4a9d-ac36-f38cae3a944d" />

cat < file2
## OUTPUT

<img width="257" height="172" alt="image" src="https://github.com/user-attachments/assets/57403d3d-188f-4a99-80c1-ebe8b2a45fef" />

# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="373" height="82" alt="image" src="https://github.com/user-attachments/assets/2790dadd-eb88-4554-8a8b-c997aee953df" />

comm file1 file2
 ## OUTPUT

<img width="327" height="282" alt="image" src="https://github.com/user-attachments/assets/9af08cc7-aa61-4a81-9387-2d17767970a3" />

diff file1 file2
## OUTPUT

<img width="317" height="317" alt="image" src="https://github.com/user-attachments/assets/e50007bb-4b52-4db3-8b64-425c8b60093c" />

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

<img width="323" height="143" alt="image" src="https://github.com/user-attachments/assets/74d87ef4-b7cd-4d1b-ae4a-83d78e9f9423" />

cut -d "|" -f 1 file22
## OUTPUT

<img width="392" height="155" alt="image" src="https://github.com/user-attachments/assets/3b87c450-446a-4473-913e-548969aab3ff" />

cut -d "|" -f 2 file22
## OUTPUT

<img width="400" height="140" alt="image" src="https://github.com/user-attachments/assets/e2255cad-db9a-4504-8612-6cc5e6cddc3c" />

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

<img width="345" height="92" alt="image" src="https://github.com/user-attachments/assets/77c6da05-0ea1-4b75-8fee-21162dcdd7eb" />

grep hello newfile 
## OUTPUT

<img width="352" height="68" alt="image" src="https://github.com/user-attachments/assets/889adf62-6618-4a90-9ba1-e492458e4b6b" />

grep -v hello newfile 
## OUTPUT

<img width="377" height="97" alt="image" src="https://github.com/user-attachments/assets/30ce4ead-74f3-4c29-b01c-2097653418fb" />

cat newfile | grep -i "hello"
## OUTPUT

<img width="456" height="96" alt="image" src="https://github.com/user-attachments/assets/f1920aa4-9d86-420f-aa20-f6262e67b64e" />

cat newfile | grep -i -c "hello"
## OUTPUT

<img width="498" height="77" alt="image" src="https://github.com/user-attachments/assets/10daddca-5ec7-44eb-b654-f582d7a0293a" />

grep -w -n world newfile   
## OUTPUT

<img width="402" height="105" alt="image" src="https://github.com/user-attachments/assets/6bae0034-f2f3-418e-9b8c-76c04af028de" />

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

<img width="461" height="98" alt="image" src="https://github.com/user-attachments/assets/b50c59f2-1fac-4755-b602-6f239afa51ae" />

egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="450" height="90" alt="image" src="https://github.com/user-attachments/assets/569892b0-ec17-4b34-9f9e-72eecfe343b5" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="498" height="95" alt="image" src="https://github.com/user-attachments/assets/63840d7d-cdd4-4075-8e7a-3f8a65815f6d" />

egrep '(^hello)' newfile 
## OUTPUT

<img width="425" height="76" alt="image" src="https://github.com/user-attachments/assets/7ec102fa-e38c-4535-b6a7-ba8e31a1156a" />

egrep '(world$)' newfile 
## OUTPUT

<img width="397" height="90" alt="image" src="https://github.com/user-attachments/assets/8347741b-3346-4313-a9c8-8d5fa8e6269f" />

egrep '(World$)' newfile 
## OUTPUT

<img width="408" height="68" alt="image" src="https://github.com/user-attachments/assets/56330263-230c-49c8-bdf7-89ae7999a735" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="442" height="117" alt="image" src="https://github.com/user-attachments/assets/be7cb870-9dba-4948-83d5-a1ffc40a082b" />

egrep '[1-9]' newfile 
## OUTPUT

<img width="368" height="67" alt="image" src="https://github.com/user-attachments/assets/93feda65-83ed-498e-966d-c849be990f87" />

egrep 'Linux.*world' newfile 
## OUTPUT

<img width="450" height="77" alt="image" src="https://github.com/user-attachments/assets/16b868ae-2bbe-46c8-855e-c938b77113c5" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="437" height="75" alt="image" src="https://github.com/user-attachments/assets/c935a45f-89d5-4e5f-8cef-3f7c7a12cf31" />

egrep l{2} newfile
## OUTPUT

<img width="353" height="92" alt="image" src="https://github.com/user-attachments/assets/bd5404ce-5420-41dd-96fd-e13caa34c226" />

egrep 's{1,2}' newfile
## OUTPUT 

<img width="396" height="120" alt="image" src="https://github.com/user-attachments/assets/d9b028a3-e5b8-4d64-bf21-ca6477c82aa8" />

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

<img width="367" height="72" alt="image" src="https://github.com/user-attachments/assets/65b07c24-e9f3-4822-88e2-9abd75ede07c" />

sed -n -e '$p' file23
## OUTPUT

<img width="382" height="82" alt="image" src="https://github.com/user-attachments/assets/9d74830a-1ff3-442f-a122-fce652cd700f" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="465" height="251" alt="image" src="https://github.com/user-attachments/assets/9673ff82-37ad-4bdf-95a4-8a095f017f97" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="461" height="243" alt="image" src="https://github.com/user-attachments/assets/9ca71c24-05cb-4c64-8a81-2d6c05b79ecc" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="477" height="250" alt="image" src="https://github.com/user-attachments/assets/98d6c95b-ce9b-47a6-ba34-7f6090cf6e5a" />

sed -n -e '1,5p' file23
## OUTPUT

<img width="410" height="163" alt="image" src="https://github.com/user-attachments/assets/e9275819-09a9-4ced-b191-b4af0763c96c" />

sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="428" height="120" alt="image" src="https://github.com/user-attachments/assets/3fb6768c-45fb-44dd-979a-9fd35461e6b3" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="486" height="95" alt="image" src="https://github.com/user-attachments/assets/8901e549-9c48-445f-8ae7-b76c7b89ca77" />

seq 10 
## OUTPUT

<img width="297" height="265" alt="image" src="https://github.com/user-attachments/assets/4dee1898-4274-4000-ad91-356b74d5f514" />

seq 10 | sed -n '4,6p'
## OUTPUT

<img width="376" height="113" alt="image" src="https://github.com/user-attachments/assets/ab6e1f80-d6dd-43f5-aa2a-e8978cf0aff4" />

seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="402" height="115" alt="image" src="https://github.com/user-attachments/assets/fe93239f-e107-40f3-9ef7-b7785c8e9d6c" />

seq 3 | sed '2a hello'
## OUTPUT

<img width="400" height="148" alt="image" src="https://github.com/user-attachments/assets/e51f7668-b3e4-4295-a7a3-b90a7abdcbd4" />

seq 2 | sed '2i hello'
## OUTPUT

<img width="410" height="117" alt="image" src="https://github.com/user-attachments/assets/afe2e670-207c-46de-bb8b-5bbae41e6d66" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="407" height="125" alt="image" src="https://github.com/user-attachments/assets/6fd730a9-808b-4ef3-9f1f-3a1e59baa159" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="462" height="117" alt="image" src="https://github.com/user-attachments/assets/2ea5c021-5e9f-4859-8b0f-25bf7ddeeca8" />

sed -n '2,4{s/$/*/;p}' file23

<img width="462" height="112" alt="image" src="https://github.com/user-attachments/assets/56aeafc9-b0c7-466d-b03f-43e6c5934e5b" />

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

<img width="327" height="177" alt="image" src="https://github.com/user-attachments/assets/e1710e34-09ec-4269-9c12-e97211b10a14" />

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

<img width="423" height="150" alt="image" src="https://github.com/user-attachments/assets/24a9128d-df5c-4ed4-80cc-122350309373" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="532" height="242" alt="image" src="https://github.com/user-attachments/assets/dfbc7666-2ca2-4d2b-83ce-9a44c2668962" />

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

<img width="427" height="153" alt="image" src="https://github.com/user-attachments/assets/072f8f66-73f5-4dab-b471-770f1982ae75" />

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="555" height="147" alt="image" src="https://github.com/user-attachments/assets/92af557b-fa97-4b9a-be51-585e69b76df5" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="371" height="251" alt="image" src="https://github.com/user-attachments/assets/49b79ec5-68cb-4489-8837-29bb24d28481" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="645" height="305" alt="image" src="https://github.com/user-attachments/assets/90ea3718-0d79-48e0-80b1-3fcd1f80db83" />

tar -xvf backup.tar
## OUTPUT

<img width="438" height="245" alt="image" src="https://github.com/user-attachments/assets/f15febcf-f1ff-42ce-a92c-ad0c6f2b6040" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="337" height="136" alt="image" src="https://github.com/user-attachments/assets/f1b26e03-a8c3-4bd8-9ba8-7e2f1efc720a" />

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

 <img width="503" height="865" alt="image" src="https://github.com/user-attachments/assets/5f18b88a-9bb0-4004-b7a0-6caf68eb65ba" />

 <img width="633" height="375" alt="image" src="https://github.com/user-attachments/assets/a24422fd-7351-40b8-ae38-6866dc9d1ae3" />

ls file1
## OUTPUT

<img width="247" height="85" alt="image" src="https://github.com/user-attachments/assets/cace9270-fc03-4723-ae0d-67883cff6165" />

echo $?
## OUTPUT 

<img width="220" height="67" alt="image" src="https://github.com/user-attachments/assets/2eaee883-60b1-423b-bd49-4d92cad40a26" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 <img width="252" height="73" alt="image" src="https://github.com/user-attachments/assets/fd3a4ee0-673b-447e-8819-5e2770da1d16" />

abcd
echo $?
 ## OUTPUT

<img width="302" height="87" alt="image" src="https://github.com/user-attachments/assets/716bf8e1-6d83-4461-a0df-a1c4eb600a92" />

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

<img width="411" height="200" alt="image" src="https://github.com/user-attachments/assets/5eb935d7-ee18-4859-b2c0-f2cd22dcf971" />

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="362" height="111" alt="image" src="https://github.com/user-attachments/assets/a1b4b72e-c17d-49b0-8d2c-ae329e2a5b12" />

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

<img width="388" height="80" alt="image" src="https://github.com/user-attachments/assets/f8588be0-9c7a-44bb-bdaf-e3d943e42569" />

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

<img width="428" height="90" alt="image" src="https://github.com/user-attachments/assets/75f3d21a-d389-4bea-9eec-59346788e911" />

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

<img width="393" height="127" alt="image" src="https://github.com/user-attachments/assets/4265dd85-b1a3-4ed7-9c44-86b9f37ff23d" />

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

<img width="422" height="133" alt="image" src="https://github.com/user-attachments/assets/2282ae43-edf0-483e-893c-86064364ca05" />

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


<img width="430" height="182" alt="image" src="https://github.com/user-attachments/assets/eed0bd3b-2afc-4156-b6f6-e5b20c46c2ea" />

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

<img width="438" height="110" alt="image" src="https://github.com/user-attachments/assets/e7da6b6c-28d3-4001-9ecc-ef711f1532d4" />

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


 <img width="631" height="256" alt="image" src="https://github.com/user-attachments/assets/9f7b6e49-0545-4c30-82f9-e552a3b86a9f" />

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
 
<img width="377" height="305" alt="image" src="https://github.com/user-attachments/assets/9369ef96-527a-4db3-96d4-4e242fd4ff7e" />

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
 
<img width="435" height="160" alt="image" src="https://github.com/user-attachments/assets/5747fa6f-77de-41dc-8cd7-a052b84c7629" />

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
 
<img width="390" height="210" alt="image" src="https://github.com/user-attachments/assets/e1710d04-cf84-462f-9c36-83a765d66000" />

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

 <img width="377" height="151" alt="image" src="https://github.com/user-attachments/assets/c953ad62-11f2-4cec-a481-c93fd64ed5d8" />

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

<img width="377" height="151" alt="image" src="https://github.com/user-attachments/assets/d317e5d5-4a87-4ccb-aa88-ac8781468ad6" />

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

 <img width="405" height="218" alt="image" src="https://github.com/user-attachments/assets/0c1caf51-357d-4f59-89d2-7813820867ed" />

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

<img width="385" height="210" alt="image" src="https://github.com/user-attachments/assets/4b312e50-6134-404e-9b36-b9cdee0c1e9a" />

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

<img width="298" height="71" alt="image" src="https://github.com/user-attachments/assets/1baaf53e-e611-40da-a30b-c56a9e050819" />

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

<img width="393" height="200" alt="image" src="https://github.com/user-attachments/assets/4bf74005-ea46-428d-861f-e7abb63c1993" />

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

<img width="392" height="191" alt="image" src="https://github.com/user-attachments/assets/793f73b0-89b9-45af-9646-6c8f1b477ddb" />

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

<img width="437" height="335" alt="image" src="https://github.com/user-attachments/assets/5eb45df8-8a3d-47c0-8152-3998346207f4" />

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


<img width="393" height="142" alt="image" src="https://github.com/user-attachments/assets/726fb202-9a62-4aa4-b174-c06f341f1a8c" />

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

 <img width="412" height="182" alt="image" src="https://github.com/user-attachments/assets/6e45610a-37b7-4845-b3c1-27122d89cc05" />

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

<img width="440" height="126" alt="image" src="https://github.com/user-attachments/assets/f277def5-74cc-48f1-adc5-9b4b62c276c1" />

cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT


<img width="408" height="127" alt="image" src="https://github.com/user-attachments/assets/f8f005fb-a24e-4b6a-91ab-accc01035cfd" />


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

 
 ./funcex.sh 1 2

<img width="376" height="97" alt="image" src="https://github.com/user-attachments/assets/16bebf76-86bd-445e-bc85-d6038e1bad68" />

 
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
$ ./argshift.sh 1 2 3

 <img width="396" height="143" alt="image" src="https://github.com/user-attachments/assets/2b6cd557-cbc7-4454-a6e2-3c38addcc7b8" />

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
 
<img width="405" height="142" alt="image" src="https://github.com/user-attachments/assets/c486c6f3-ab3f-479c-9041-bcaaaf01003b" />

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

<img width="407" height="138" alt="image" src="https://github.com/user-attachments/assets/be33651b-3019-4ad8-9e70-6f9069e635fb" />

# RESULT:
The Commands are executed successfully.
