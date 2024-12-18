This challenge is basically to test knowledge of linux commands. I will try as much as possible to make it short and understandable.

PS: As i solve the challenges, I add.

# LEVEL 0

For this level, we login with the credentials given.

username: bandit0   

password: bandit0 

host: bandit.labs.overthewire.org  port: 2220

![image](https://github.com/user-attachments/assets/7123ddaa-cde1-4035-81a9-d3004c44160f)

We use the command ```ls``` to view files and we found a readme file. Viewing it gave us our password. 

![image](https://github.com/user-attachments/assets/0b39b94d-0e10-40b4-89e6-f5ac1eeb1eff)

# LEVEL 1

Credentials...

Username:bandit1  

password:ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

After successfully logging in we saw a '-' file and we are not able to cat it. After little reasearch we found out that to cat a dash file you need to add './'

![image](https://github.com/user-attachments/assets/2608547d-4f84-47d1-816b-15594df1724d)

# LEVEL 2

username: bandit2   

password:  MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

![image](https://github.com/user-attachments/assets/69d6bdcf-6d6e-4d19-bd7b-64855f2a36fe)

We use the tab key for autocomplete because of the spaces in the file name.

# LEVEL 3

username: bandit3    

password: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

listing files in our current directory

![image](https://github.com/user-attachments/assets/94ddee54-f457-4d94-9f53-0abe8be10aa2)

we found a directory there so we navigated into it. We tried listing files there but it was like there was nothing, we moved on to check for hidden files and as we will have it, we saw something trying to hide from us hehe.

![image](https://github.com/user-attachments/assets/fd89e9d2-a607-4aa2-97ec-f463393605d3)

viewing the file

![image](https://github.com/user-attachments/assets/ed7b0227-3602-4471-a20f-71028bb56c82)

# LEVEL 4

username: bandit4    

password:  2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

listing files in our current working directory, we found a dir, inhere. We navigated into it and found a number of files. 

![image](https://github.com/user-attachments/assets/f8b1faee-6fb5-4892-9cab-14b5bc36b600)

For ease, we use the <file> command to view what type of files they are. I tried to use wildcard but it gave error. 

![image](https://github.com/user-attachments/assets/c54a9c99-9543-4b45-8862-6491cd81ea37)

I remembered they are all dash files so i used ./* instead of just * and boom!!!, it came to us.

![image](https://github.com/user-attachments/assets/f73fe092-1154-4434-a502-d3310d4e9756)

To view the file we use normal ```cat``` and then we get the password for the new level.

![image](https://github.com/user-attachments/assets/465be3da-99f8-4cf3-b30b-8703633452cd)

# LEVEL 5

username: bandit5    

password: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

After we successfully logged in, we navigated to inhere directory and saw many other directories. To save time and stregnth we use the ```find``` command.

![image](https://github.com/user-attachments/assets/218f2d5b-caa6-4e72-9dca-1f9d927ab472)

Using the ```find``` command with the parameters given already, the search became easy and we found our file...

![image](https://github.com/user-attachments/assets/41c85cf3-ec23-4d04-bd0a-d19034c26083)

# LEVEL 6

username: bandit6  

password: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

After we logged in, we tried to list files and we could not find anything not even hidden files. We read the instructions again and they said it was somewhere on the server so we just went ahead to use the ```find``` command.

![image](https://github.com/user-attachments/assets/25564ea1-81b0-404d-96df-16d3a81efd2d)

We narrowed our search with that ```2>/dev/null``` thing and we got a place where the next password is. I copied the path and catted it out.

![image](https://github.com/user-attachments/assets/a8d05a39-6f2c-4554-927b-d91c76ec59c0)

# LEVEL 7

username: bandit7   

password: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

We list the contents in our working directory and we see a .txt file, catting it will give one kain long novel so we just used ```grep``` to look for the word. Very easy for us to get the password.

![image](https://github.com/user-attachments/assets/5fdf477d-742e-49ee-89ba-663f3b6c7477)

# LEVEL 8

username: bandit8    

password: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

For this level, we were also told that the password is in a file called data.txt. But in this case, almost each line is repeated as shown below using sort command:

![image](https://github.com/user-attachments/assets/fa6f3dbd-d33a-4258-a10e-c9f0c395de70)

As you can see the end of the file are arranged. We will be piping the sort command with ```uniq``` and indicating we want just unique lines using the -u flag which tells it to show only unique lines

![image](https://github.com/user-attachments/assets/44a1f3b4-e731-49b4-8d8a-b4a2c78d7965)

# LEVEL 9

username: bandit9  

password: 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

We were given a file that is not an ASCII text. If we try to cat it, we get strings of data and we can't even grep. So we wil use strig command and then ```grep``` '========='

![image](https://github.com/user-attachments/assets/1e17faf7-6f37-4ff5-a19e-c8cf379f7701)

# LEVEL 10

username: bandit10  

password: FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

After successfully loggin in, we found a data.txt which was an ascii text. As we catted it, we saw it was an encoded message in base64. We can either use an online tool or we use the ```base64``` command. 

SYNTAX: ```base64 -d "name of file"```. The -d flag is to decode

![image](https://github.com/user-attachments/assets/61802453-66d4-473b-9d9e-974c1fb67bbd)

# LEVEL 11

username: bandit11   

password: dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

For this, we were also given a file that contained set of characters we can't pronounce. We realize it is also a cipher text and it was rotated 13 times. We can either do this using ```tr``` command or we use an online tool. I would have preferred not to use terminal but as per this game is supposed to help make us better and more familiar with linux commands, I won't be using the online tool. We can as well do it manually...that one will stress you small sha, just move each character 13 times. 

![image](https://github.com/user-attachments/assets/5700e16e-c65c-4675-b71c-e4e90685707d) 

OR

![image](https://github.com/user-attachments/assets/5b3720ff-c3ad-4dc6-af38-88848687feff)

And boom!, we have our password.

# LEVEL 12

username: bandit12 

password: 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

We were given an instruction to follow here first,and we were also told the file we are dealing with is a hexdump data which was repeatedly compressed.

![image](https://github.com/user-attachments/assets/21ffdc8b-4e8d-434f-9194-cf6d9ce10bb5)

Following the instructions, we will create a dir in /tmp and copy the data there and then we start to decompress till we get our password.

![image](https://github.com/user-attachments/assets/b938ec43-12bb-46b8-882b-89be624914fd)

After moving, we use the ```xxd``` command with -r flag to revert the hexdump data alongside the name of the new file we want to save it in and then what type of file it is to know what tool to use to compress it.

NB: NOW IS THE TIME TO MAKE ```man``` YOUR BESTFRIEND. 

![image](https://github.com/user-attachments/assets/4a15c541-ad8c-4770-ab52-36e2ba9c5d13)

From here, what we will keep doing after decompressing is to check the file type, change the file extension to whatever it shows as what type of file it is i.e this was showing gzip file so i renamed it to data.gz.

![image](https://github.com/user-attachments/assets/a04b989b-9855-48bf-a1da-c4694a0c8606)

After decompressing the first one, i got a bzip2 file, i used my manual page again after renaming and decompressed to get a gzip file again

![image](https://github.com/user-attachments/assets/158c19d2-422f-4e27-bc1b-4fcf73888232)

We keep repeating the process till we get a kind of file that is human readable. It will most likely be our password.

![image](https://github.com/user-attachments/assets/e4e682ee-c7cc-4760-a32a-d7dc6ca0d1bc)

After several decompression and reversion we were able to get a human readable file and we saw that it was our password for the next level.

![Screenshot from 2024-08-08 02-19-28](https://github.com/user-attachments/assets/06d47c29-c621-4f02-8056-98604166b552)

# LEVEL 13 and 14

username: bandit13    

password: FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn 

The instruction here stated that the password can only be read by user14. We need to find a way to login as bandit 14. I checked for files in my directory and found a ssh key there. It can be used in place of a password, what you just need is the username

![image](https://github.com/user-attachments/assets/f61e6033-2b98-4080-a96a-cac4088e9b09)

I created a file on my host machine and saved the private key in it. 

![image](https://github.com/user-attachments/assets/08c38448-2502-4754-82a5-ef612e94e5b9)

I will proceed to login into user14 with the key i found. After trying, I got an error, apparently, i need to change the permission of the private key.

syntax: chmod 600 <name of the privatekey>

![image](https://github.com/user-attachments/assets/fabfb8ea-da77-40f8-9189-35ea848c138c)

After changing it, we successfully logged in, now we need to navigate to the directory where the password for the level is stored. We get the password to bandit14 there.

![image](https://github.com/user-attachments/assets/0b0cbb2c-a94d-49de-a99b-d42f513e8871)

# LEVEL 14    

username: bandit14      

password: MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS

For this level, we will be able to get the password to the next level by submitting the password we retrieved in the last level to port 30000 on localhost. We can either use local host or use 127.0.0.1 for this, both works. 

![image](https://github.com/user-attachments/assets/5b8b16c7-5264-42c2-bd2f-d2f5d81b91f8)

As you can see, both ways gave same password. We meauve

# LEVEL 15       

username: bandit15         

password: 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo

For this level, we will also be submitting the old password to get the password for the next level, this time they gave a different thing.

![image](https://github.com/user-attachments/assets/8dabfa18-1a1f-4745-89c8-68d51f365c55)

I just connected the localhost server woth the openssl clinet and pasted the password from this level since they told us it was using ssl encryption.

# LEVEL 16 

usernmae: bandit16          

password: kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

For this level, we need to know which and which ports are opened as they gave us a range so we will be using the ```nmap``` tool. It is known as network mappper, it can do alot of things such as network scanning, OS detection, host discovery etc. The syntax for this is ```nmap <ip address>```. Other flags can be attached depending on what you want to do with the scan. You can use the man page to read more.

![image](https://github.com/user-attachments/assets/3ee896d9-40d4-48ea-b985-f35d2cd77e44)

After running the scan, we were gicen a number of opened ports but we don't know what service we are running on so we add the -sV flag for it to give us that. Reason for this is so we can know theport that has a listener on it.

![image](https://github.com/user-attachments/assets/f51e0991-2e08-4460-aa83-7a34386ae5a3)

We have 5 ports running here, our best guess is 31790 so we will try to connect to that using openssl using the same format.

For this we will be using the ```ncat``` command. The syntax is, ```ncat --ssl localhost 31970```

After doing that, we paste the password for this level and then we get a RSA Key. The key can be used to login into the next level whic is bandit 17 just like we did in level 14.

# LEVEL 17 

username: bandit17       

password: EReVavePLFHtFlFsjn3hyzMlvSuSAcRD

After successfully logging in, we wil find the password for this level wehre passwords are being stored. 

![image](https://github.com/user-attachments/assets/4cf630e8-e7a6-4159-ac01-8c98d633883e)

Now we were told there are two different passswords, I actually do not know what command to use. They gave a list of commands as usual and there was this one i was unfamiliar with. After a little research, It was what i eventually used. 

After listing the files in our current working directory, we see two different files, when i view both files, I see they look so familiar so i used the ```diff``` command to check for the difference. Our password should be in the ```password.new``` so we look out for that. 

![image](https://github.com/user-attachments/assets/eae64af7-74f2-41ff-a6f7-2ef901bb7a7d)

And boom! we found our password for the next level

# LEVEL 18

username: bandit18    

password: x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO

Unfortunatly for us someone modified the .bashrc file to keep logging us out.

![image](https://github.com/user-attachments/assets/a9cf92d5-ca25-48e3-8d72-cc96e8e808e8)

After seeing i won't be able to login, i decided to run command with ssh instead of running it when i am logged in. Since we were told there was a readme file there, we ```ls``` to view the files and the we ```cat``` it after.

![image](https://github.com/user-attachments/assets/2857c77c-60c4-40e7-96ae-d445b3b0ce06)

We now have our password for the next level.

# LEVEL 19

username: bandit19      

password: cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8

After successfully logging in, i tried to check the password in the ususal place but it says permission denied. So i followed the instruction given and read a little about setuid. First we need to check which user can run the file that was given, for that we use ```ls -l``` 

![image](https://github.com/user-attachments/assets/13260fea-0f53-48f9-90c2-e4e3b125f6a5)

I then tried to execute the file to see the usage and it gave me one. I followed it and it became clearer, I could run this as bandit20 so it was possible for me to check the password and not get a permission denied.

![image](https://github.com/user-attachments/assets/8dff0a7d-6f66-496d-8310-1e26fe7e2f46)

I did just that and it gave me this

![image](https://github.com/user-attachments/assets/e2afd225-2edb-48da-b1ed-22435dcfcbf3)

# LEVEL 20

username: bandit20         

password:  0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO

Reading the level goal, I realized I will be needing netcat to listen and then paste password somehow. I proceeded to opening another tab. I will be listening on one of them and executing the setuid file on the other.

![image](https://github.com/user-attachments/assets/36d121a8-3a0a-4b72-8530-a943acdd9d96)

After multiple trials, it gave me the password for the next level.

![image](https://github.com/user-attachments/assets/49e2e4ed-cbf3-44a0-a286-dd7be962b7fe)

# LEVEL 21

username: bandit21           

password: EeoULMCra2q0dSkYj561DX7s1CpBuOBt

After successfully loggging in, we follow the goal that was given to check for cronjobs. We will be checking the ```/etc/cron.d``` to see the program that is running immediately.

![image](https://github.com/user-attachments/assets/b6135cf2-74ea-47ab-beb5-9df93f874b94)

As we can see, we have a file called cronjob_bandit22, we will try to see the content of the file for any hints.

![image](https://github.com/user-attachments/assets/eab7a648-e45e-468e-ba21-ef22c6f07b1f)

We have a bash file running /usr/bin. We will navigate into there and view the conent of the bash file. 

![image](https://github.com/user-attachments/assets/d9bddc59-a02c-4258-89b3-3bbe5e7d699c)

From the bash file, we see that everyone has priviledge to read /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv and the password for the next level is written there. So we will just view the content of this file and hope to see our next password there.

![image](https://github.com/user-attachments/assets/af20cad2-1460-4702-9a5a-db223fcd09b5)

# LEVEL 22             

username: bandit 22            

password: tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q

For this level, we were also told that we have processes running on the same path as the previous level. A script is also running and it will be our hint for the next password. Following the same process as the previous level, we found our script but this time the content is a bit different. 

![image](https://github.com/user-attachments/assets/84e54938-95b5-4bf4-805e-e892fb3f2959)

The code here is looking self explanatory so we will just follow and use logic as the spirit leads....

![image](https://github.com/user-attachments/assets/f32f591c-e0a8-486d-afbe-6f6d3045e573)

And we got the password for the next level.

# LEVEL 23 

username: bandit23            

password: 0Zf11ioIjMVN551jX3CmStKLYqjk54Ga

We were givn a task related to cron job and the same process for the last two levels would be followed again. 

After checking this, we see that the bash file here is quite differnet from others we have been seeing and this is a bit confusing and it even contained a for loop. 

![image](https://github.com/user-attachments/assets/0be1580b-2fab-4bba-b22b-d1352fc867f3)

For this level, we will need to create a script that can be executed by user bandit 24 and what the script will do is to print the password to a directory we can read from. 

First we will create a new directory in the /tmp directory where we will be writing our script. 

![image](https://github.com/user-attachments/assets/d7768b4e-21a0-45a2-b4d9-379550823dfd)

```
#!/bin/bash

cat /etc/bandit_pass/bandit24 > /tmp/bangis/bangis.txt
```
After that, we grant execution permissions to the script and then we copy it to the specified directory from the cronjob's script i.e /var/soppl/bandit24/foo and then we wait for about a minute to get bangis.txt where our password will be stored.

![image](https://github.com/user-attachments/assets/349dd90f-7c76-4bd2-8ad4-ed4e9d3dea99)

# LEVEL 24

username: bandit24

password: gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8

When I saw the task for this level, first thing that came to mind was to find a way to use crunch to get all combination and use awk to input the password behind every combination. It would have worked except there was not crunch installed and we were not able to use wget. I decided to use a bash script to get the job done.

```
#!/bin/bash
prev_pass="gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8"
for i in $(seq -w 0 9999); do
    result="${prev_pass} ${i}"
    echo "$result"
done
```
THe above bash script will print out the password and the combination starting with 0000 until 9999. We then run a listener together with it.

![image](https://github.com/user-attachments/assets/d18a6730-a9e3-4d51-a557-76c75ce852f1)

After getting alot of incorrect password, we eventually got our password. 

![image](https://github.com/user-attachments/assets/98a74683-1c99-4b11-af32-0f5092587e6a)


# LEVEL 25 AND 26

username: bandit25

password: iCi86ttT4KSNe1armKiwbQNmB3YJP3q4

We won't be having any need to get the password for this level, this is beacause we get an id_rsa file to login to the next level. After successfully logging in, list the files in the current directory and you see the file, login to the next level which is bandit27 directly from the local machine.

![image](https://github.com/user-attachments/assets/ca010253-06b5-4ec7-84b6-d89800914a56)

We notic we get an output different from the others and we also get logged out, from the level goal we know that this level might not be operating on the normal shell i.e /bin/bash or /sh. We check the /etc/passwd file to see what shell it runs on.

![image](https://github.com/user-attachments/assets/85315df4-1e24-49b0-b14f-112662c5ae16)

As we can see it is runs on a differnet shell, good for us we can read it as see what it does. From the shell file, it shows that we exits the shell onece logged in and there is a text file, we can get a shell from that text file. When you we log in the text file will cat itself using ```more```. What we need to do is to reduce the terminal size so the entire text won't show and from there we can get a bash shell

![image](https://github.com/user-attachments/assets/9b774946-c58a-48d6-9f16-d0fc288ea778)

Thaat's the size of my terminal, small and messy hehe. We get a more shell where we can use 'v' to type commands. From here we set our shell to bash using ```:set shell=/bin/bash``` and we spawn our shell using ```:shell```. Boom we are logged into bandit26. When we list the files in our direcrtory, we see a setuid executable file, this can be used to read the password of the next user. 

![image](https://github.com/user-attachments/assets/9b8d67df-390f-4c90-b629-4033823d10f4)

# LEVEL 27

username: bandit27

password: upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB

For this level, we will be dealing with the git command as it is the only command provided for us. We were given a repo to clone and we will do just that using the git command. First we need to create a new dir in the /tmp folder and clone it to that new dir using the password for the level.

![image](https://github.com/user-attachments/assets/e987b2bd-6b7c-4a7d-b3c0-a45808156660)

We move into the new dir and see the files. We find a file there and when we view the content of the file, we find our next password there.

![image](https://github.com/user-attachments/assets/cf2681c3-4398-439c-a608-fd67041edf97)

# LEVEL 28

username: bandit28

password: Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN

For this level, we will be cloning the repo for this level just like we did or the past level. We have a README.md file, when we try to view it, what we get is xxxxxxxx as the password. Obviously that can't be the password. Knowing that .md files can be changes, we look for a way to check for past changes using ```git log``` 

![image](https://github.com/user-attachments/assets/bc7e5de1-f4ab-47a9-9e42-2c86d9596ea7)

Using ```git checkout id```, we can restore the in itial state of the file using the strings of characters which is out commit id. There are three ids there, we use the second one to get the new password. 

![image](https://github.com/user-attachments/assets/633ada6c-070d-4915-946e-ba67cd287de8)


# LEVEL 29

username: bandit29

password: 4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7

For thie level, we will still be dealing with git. After successfully logging in, we make a new direcroty in the /tmp dir and clone the repo there just like the other levels using the level password. After cloning we nothing something in the README.md file.

![image](https://github.com/user-attachments/assets/4c810a1c-61f8-4b7c-9462-5fa7a9d3e72f)

Seeing a "no password in production" might give us a hint that there are other productions so we decided to check all branches and then check the logs in those branches.

![image](https://github.com/user-attachments/assets/4c1805d1-8860-44f9-8ad2-63b7cb1416c4)

We are in the mater branch presently, so we will move to check the dev branch to see what it has in store for us using the ```git checkout <brank-name>``` and then we check the log again.

![image](https://github.com/user-attachments/assets/c2820096-b7c9-4c09-a907-0891a44d5265)

Upon checking the first log, we got what we have been searching for.

![image](https://github.com/user-attachments/assets/fa315636-f834-44f5-91fe-212dfe5826b8)



# LEVEL 30

username: bandit30

password: qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL

After logging in, we do the norms which is cloning the repo. This time, the README.md file we found there was very different from the others. This one said something that got me scared. It says it's just am empty file and it laghed, more like we are wasting time. I decided to just do the normal things i did in the last two levels but nothing so I went back moving around and checking for hidden stuffs. We found a hidden directory and decided to enumerate it. To my greatest suprise, I found a branch with a log and it was names secret. Immediately, I knew I was getting somewhere good.

![image](https://github.com/user-attachments/assets/9ea674cd-a26c-4edc-b9a0-41023cd690fd)

I just jejely used my git show command to check what it has for us and...Ladies and Gentlemen, we have our next password.

![image](https://github.com/user-attachments/assets/68b33e46-ec17-4aa0-a8c1-6f5e56676596)



# LEVEL 31

username: bandit31

password: fb5S2xb7bRyFmAvQYQGEqsbhVyJqhnDy

Still on git, this time our README.md file asked us to push a file with instructions.

![image](https://github.com/user-attachments/assets/de6aa556-05c6-43f6-885b-0030c3e0b1dc)

First, we create the file we were asked to with the necessary inputs and then we tried to add the file we just created by using ```git add```. Little did I know it was not that easy,but they give us some hints.

![image](https://github.com/user-attachments/assets/2bb0d79f-7b97-4920-9623-2e2ecb249fc5)

There are two ways to go about this, either to delete the gitignore file or use the flag . The easier one for me is to just use the flag that was given.

We did that and it was a success, so the next thing is to commit our changes, and we got a response to use git push. 

![image](https://github.com/user-attachments/assets/2e586a5f-f17f-44a4-8222-c58f8804abc1)

Ladies and gentlemen...our next password.


# LEVEL 32

username: bandit32

password: 3O9RfhqyAlVBEZpVb6LYStshZoqoSx5K


# LEVEL 33

username: bandit33

password: 3O9RfhqyAlVBEZpVb6LYStshZoqoSx5K


