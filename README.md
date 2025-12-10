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
<img width="238" height="154" alt="image" src="https://github.com/user-attachments/assets/f702ea48-2638-4603-b953-a1baf984a363" />




cat < file2
## OUTPUT
<img width="200" height="171" alt="image" src="https://github.com/user-attachments/assets/ebc1b74d-5980-4fa0-bb2f-b40cd3ceea03" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="348" height="78" alt="image" src="https://github.com/user-attachments/assets/a60c2c36-bea8-43b8-a8b0-5b6816bb2371" />

 
comm file1 file2
 ## OUTPUT
<img width="310" height="218" alt="image" src="https://github.com/user-attachments/assets/bfcea647-a685-4894-963e-9b100f5b4971" />

 
diff file1 file2
## OUTPUT
<img width="278" height="274" alt="image" src="https://github.com/user-attachments/assets/404a2940-0014-4873-94ba-2b60e59aeb8b" />



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
<img width="226" height="100" alt="image" src="https://github.com/user-attachments/assets/74b80b4e-ee8e-4956-ae17-aecd45d0d835" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="308" height="126" alt="image" src="https://github.com/user-attachments/assets/6ae723e7-0ede-4e2c-a3ea-009669248d30" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="291" height="120" alt="image" src="https://github.com/user-attachments/assets/84e46c9c-27bb-4891-ad67-cbc8252ba090" />


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
<img width="276" height="67" alt="image" src="https://github.com/user-attachments/assets/f71a0f06-0882-49de-bd79-009d8baacdee" />



grep hello newfile 
## OUTPUT
<img width="272" height="72" alt="image" src="https://github.com/user-attachments/assets/937d9f85-4746-4369-9940-19a8edeb4dc8" />




grep -v hello newfile 
## OUTPUT
<img width="288" height="77" alt="image" src="https://github.com/user-attachments/assets/71a8ce43-e476-452e-9ab0-c796b986ae16" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="401" height="103" alt="image" src="https://github.com/user-attachments/assets/747cfe0d-4b92-48f4-9a94-c328c1b4a4b1" />





cat newfile | grep -i -c "hello"
## OUTPUT
<img width="404" height="84" alt="image" src="https://github.com/user-attachments/assets/255a28e7-953e-4294-aa97-7d2ab6ff7018" />




grep -R ubuntu /etc
## OUTPUT
<img width="1008" height="589" alt="image" src="https://github.com/user-attachments/assets/5cd898c8-5849-42fa-8a23-351b097959d7" />



grep -w -n world newfile   
## OUTPUT
<img width="313" height="94" alt="image" src="https://github.com/user-attachments/assets/1540452c-f132-4a53-b0dd-f5e56f92e66a" />


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
<img width="391" height="103" alt="image" src="https://github.com/user-attachments/assets/98a02176-17f5-4200-8284-3ca36f7ec5d1" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="380" height="100" alt="image" src="https://github.com/user-attachments/assets/467866ba-2c2c-4bc3-ade7-eed73c0ff334" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="425" height="99" alt="image" src="https://github.com/user-attachments/assets/c6ad3645-3e03-48fa-8863-ed003a00e382" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="341" height="70" alt="image" src="https://github.com/user-attachments/assets/930ea586-84df-4a0e-9530-0e2ac8216cfe" />



egrep '(world$)' newfile 
## OUTPUT
<img width="332" height="95" alt="image" src="https://github.com/user-attachments/assets/5a676cdd-af56-4225-9d73-14acd0d0f74c" />



egrep '(World$)' newfile 
## OUTPUT
<img width="317" height="74" alt="image" src="https://github.com/user-attachments/assets/3edd7dca-32dc-4e32-b4d1-016dbd7fbb4b" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="383" height="123" alt="image" src="https://github.com/user-attachments/assets/14c2f0dc-3124-4cbe-a76b-fe9785ec2b56" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="318" height="73" alt="image" src="https://github.com/user-attachments/assets/eeeaa408-e20e-4c59-ae25-754664fad03b" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="377" height="79" alt="image" src="https://github.com/user-attachments/assets/55120ec6-ff49-4dc8-b9eb-a4fd354d5fc7" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="364" height="78" alt="image" src="https://github.com/user-attachments/assets/4c932536-5aef-417f-bcdd-f2955eb832ea" />


egrep l{2} newfile
## OUTPUT
<img width="327" height="94" alt="image" src="https://github.com/user-attachments/assets/c7af41e8-e373-4962-aae1-2d70e5e9b424" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="364" height="121" alt="image" src="https://github.com/user-attachments/assets/80166119-6e57-4de4-a249-1cc52d87d23d" />


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
<img width="328" height="78" alt="image" src="https://github.com/user-attachments/assets/eb2a1bed-2fb2-4d8f-aab2-96f8469b41d7" />



sed -n -e '$p' file23
## OUTPUT
<img width="305" height="74" alt="image" src="https://github.com/user-attachments/assets/39f8dd1f-aeeb-42b6-a24c-58466a52f8a4" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="371" height="245" alt="image" src="https://github.com/user-attachments/assets/1de3fc60-7a70-4e18-a598-e077356193ef" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="430" height="247" alt="image" src="https://github.com/user-attachments/assets/81582d4c-c1f6-44c1-894b-33f985561b2c" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="402" height="247" alt="image" src="https://github.com/user-attachments/assets/a93f3c53-64da-48e1-8efd-8aeea75195ef" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="338" height="175" alt="image" src="https://github.com/user-attachments/assets/bac1fad9-ed25-4744-9d1d-17ea1ffabf6a" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="387" height="126" alt="image" src="https://github.com/user-attachments/assets/2947c436-2222-4b4c-9105-0df11e89441a" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="427" height="99" alt="image" src="https://github.com/user-attachments/assets/6513e0e9-fb50-42f2-9ba7-c56b83ef06ed" />



seq 10 
## OUTPUT
<img width="261" height="297" alt="image" src="https://github.com/user-attachments/assets/906cb355-8ec4-4631-8633-2282848cab1b" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="355" height="128" alt="image" src="https://github.com/user-attachments/assets/68343088-5e56-42ef-8090-501b7fcff024" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="330" height="125" alt="image" src="https://github.com/user-attachments/assets/2eea1d24-3f4e-40d1-b644-1917e736f11e" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="320" height="147" alt="image" src="https://github.com/user-attachments/assets/5b863ada-d678-48d1-8207-ba4f51ab7dbe" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="322" height="123" alt="image" src="https://github.com/user-attachments/assets/bf7b4027-2ba5-4d18-abde-b925b3b5a2b6" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="327" height="127" alt="image" src="https://github.com/user-attachments/assets/fc21d45d-2e5d-4ead-b6de-46a94e11bbb5" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="380" height="127" alt="image" src="https://github.com/user-attachments/assets/1734d26b-5c0f-4842-ab36-48687d9d69a0" />



sed -n '2,4{s/$/*/;p}' file23

## OUTPUT
<img width="417" height="127" alt="image" src="https://github.com/user-attachments/assets/019e09b9-3f1b-40e1-a60b-8d1e494c903b" />




## Sorting File content
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
<img width="339" height="179" alt="image" src="https://github.com/user-attachments/assets/1bdb8ef5-5935-42bc-9234-3369475dac08" />


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
<img width="315" height="169" alt="image" src="https://github.com/user-attachments/assets/885402b2-a59d-424e-a067-907311d964f8" />



## Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 <img width="441" height="254" alt="image" src="https://github.com/user-attachments/assets/6020d37b-cc6d-4714-b12b-4b1d1ddf6d41" />


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
<img width="357" height="124" alt="image" src="https://github.com/user-attachments/assets/50d131ab-b609-4bb9-a9fe-ba8ba9b62a0e" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="459" height="123" alt="image" src="https://github.com/user-attachments/assets/458bdff8-4536-4a7f-94a0-7d3da83db7b0" />



## Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="430" height="879" alt="image" src="https://github.com/user-attachments/assets/cd514223-0b3e-484f-b662-0edbf50e54a7" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="733" height="975" alt="image" src="https://github.com/user-attachments/assets/c9f38b90-ff49-493d-8292-065e3037a6df" />


tar -xvf backup.tar
## OUTPUT
<img width="497" height="874" alt="image" src="https://github.com/user-attachments/assets/fbcfa170-586b-40dd-ad1d-57511c0e1551" />

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
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
##OUTPUT



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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


# RESULT:
The Commands are executed successfully.
