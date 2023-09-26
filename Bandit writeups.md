# BANDIT OVER THE WIRE WRITEUPS                                               

It took me awhile to actually install linux. and i used it as a VM,
Oracle VM Virtualbox, i installed Kali linux and used it to do the tasks

## level 0: 
I had little trouble connecting to ssh becuase i didnt know the
format of connecting to the port, once i found that out i was able to
get into it(ssh bandit0@bandit.labs.overthewire.org) with the password
bandit0 PASSWORD FOR LEVEL 0:Bandit0

## level 1:
- logged into bandit0 server, using the password bandit0 given
- the password was supposedly stored in a readme file
- searched for the readme file using ls command
- then used cat command to read the contents, and inside was the password: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
## level 2:
- logged into bandit 1 server using the previously obtained password
- the password was stored in a file called -located in home directory
- searched for the file using ls command
- then used cat "./-" to read the file since it has a hyphen, and got the password:rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
## level 3:
- logged into bandit 2 server using the periously obtained password.
- password was stored in a file called spaces in this filename.
- searched for the file using ls command
- used cat'spaces in this filename' to get the pasword:aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
## level 4:
- logged into bandit3 server
- password was stored in a hidden file in the inhere directory
- first, i changed my directory to inhere, by cd inhere
- then listed the contents by ls -al
- then after seeing the file, i typed cat .hidden to get the password:2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
## level 5:
- logged into bandit4 server
- password for the next level is stored in the only human-readable file in the inhere directory
- used cd inhere, and ls to list all the files in the inhere
- read a bit about find command, and found that it can show what type of data is within the file
- used find . -type f | xargs file and foound that file07 had ASCII text
- then used cat ./-file07 and got the password:lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
## level 6:
- logged into bandit 5 server
- The password for the next level is stored in a file somewhere under the inhere directory, under conditions,human-readable,1033 bytes in size,not executable
- since i had read about the find command before, i was able to sort and file the file by using conditions
- after ls, and cd inhere to get into the dirrectory, i used the conditions, find . -type f -size 1033c(bytes) and i got the file
- used cat command on the file foudn the password:P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
## level 7:
- logged into bandit 6
- The password for the next level is stored somewhere on the server, with the condtions, owned by bandit7, owned by group bandit 6, and 33 bytes
- since its anywhere on the server, i used "find /" to search the entire system, then continued with "find / -type f -user bandit7 -group bandit6 -size 33c
- then it displayed a lot of files, where on of the files had the name "password in it
- used cat on it and got the password:z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
## level 8:
- logged into bandit 7
- used ls -alps command to get all the files listed and found the "data.txt".
- used the cat command to get a whole list.
- then i read about strings command, found that it sorts out the word u mention with it.
- i used it with grep "strings data.txt | grep "millionth" and got the password next to the word.
  password:

## level 9:
- logged into bandit 8
- used ls to find all fles, found data.txt
- used cat data.txt to read te contents and inside was just a huge text paragraph
- then i found that those were duplicate passwords and so i leanred about the "sort" command given in the 
          hint, and used it( sort data.txt), this sorted all alike passwords together
-  then i found one password which was only repeated once, which ultimatly was the password
password:

## level 10:
- logged into bandit 9
- The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.
- since "="is special condition, i greped it with strings
- i used "strings data.txt | grep "=", and got he password:G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

## level 10-11:
- logged into bandit 10
- The password for the next level is stored in the file data.txt, which contains base64 encoded data
- using cat data.txt, gave the base64 script
- used "base64 -d data.txt" using the base64 command, got the pasword:6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

## level 11-12:

- logged into bandit 11
- The password for the next level was stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
- so rot13 means that the password was encrypted, i had to use cyberchef, set it to rot13 and decrpyt the password that i had got after using cat on the data.txt
- The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

## level 12-13:
- logged into bandit 12
- he password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed.
- hex dump is basically a  hexadecimal veiw of computer data, from a file or memory location.
- after using cat, i read about the xxd command given in hints and found that it reverses the hex dump
- so i used mkdir /tmp/lfwe( lfwe was randomly made)
- the cp command on the address and then cd command to get into it
- used head data.txt and then used the xxd command "cat data.txt | xxd -r > data"
- data was a new file formed, used file command and mv command  to change it to data2.gz
- gzip -d data2.gz and then file data2(newly formed one), then converted data 2 into data3.bz
- this continued untill data9 and finally at data9, when i used cat, i got the password:wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
## level 13-14
- logged into bandit 13
- The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14
- using ls, found sshkey.private and then ran "ssh -i sshkey.private bandit14@localhost" in order to login in user bandit14,
- and after getting in i used "cat bandit14" after using cd on  /etc/bandit_pass/
- and got the password:fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq

## level 14-15
- logged into bandit 14
- The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.
- i ran nc localhost 30000 but it showed wrong password
- so after using "cat /etc/bandit_pass/bandit14"got the password:fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
## level 15-16
- logged into bandit 15, using the password :jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
- after reading about nc command and ssl, i used "ncat --ssl localhost 30001"
- and then got the password:JQttfApK4SeyHwDlI9SXGR50qclOAil1
## level 16-17-18:
- logged in bandit16
- The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000.
- so i used the nmap command"nmap localhost -p 31000-32000, and a column with port info popped
- the port 31790 was open, so i used ncat --ssl localhost 31790 , which shows a huge private key, i stored the key in vim, used chmod 400 (name) and then used ssh command back to enter into the bandit 17
- got into bandit17
- using diff command formt the hint, i got the new password

## level 18-19:
- using ssh -t bandit18@bandit.labs.overthewire.org -p 2220/bin/sh logged into the pseudo server
- using ls, found readme file,and cat readme yeilded the password
 
## level 19-20
- after loggin into bandit 19, i ran ls, saw file bandit20-do
- so to excute the file i used hint "./ bandit20-do command
- the output came, that i should run it as an new different user
- so i used ./bandit-do id and was able to see its info
- since the password was in /etc/bandit_pass/ idecided to run the cat address since only bandit 20 can read it and got the password
## level 20-21:
- There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument
- i ran the steuid command and for the second i tried connecting to my own network to see if it wokrs
- cat /etc/bandit_pass/bandit20 | nc -1 localhost -p 1234
- this connectes the server to level 20 and then we use./suconnect 1234 to get the password, and the other password is in the new terminal opened
## level 21-22
## level 22-23
## level 23-24
## level 24-25
## level 25-26
## level 26-27
## level 27-28

        
        

