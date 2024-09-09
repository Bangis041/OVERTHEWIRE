This challenge is basically to test knowledge of linux commands. I will try as much as possible to make it short and understandable.

PS: As i solve the challenges, I add.

# LEVEL 0

For this level, we login with the credentials given.

username: bandit0    password: bandit0  host: bandit.labs.overthewire.org  port: 2220

![image](https://github.com/user-attachments/assets/7123ddaa-cde1-4035-81a9-d3004c44160f)

We use the command ```ls``` to view files and we found a readme file. Viewing it gave us our password. 

![image](https://github.com/user-attachments/assets/0b39b94d-0e10-40b4-89e6-f5ac1eeb1eff)

# LEVEL 1

Credentials...

Username:bandit1  password:ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

After successfully logging in we saw a '-' file and we are not able to cat it. After little reasearch we found out that to cat a dash file you need to add './'

![image](https://github.com/user-attachments/assets/2608547d-4f84-47d1-816b-15594df1724d)

# LEVEL 2

username: bandit2    password:  MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

![image](https://github.com/user-attachments/assets/69d6bdcf-6d6e-4d19-bd7b-64855f2a36fe)

We use the tab key for autocomplete coz of the spaces in the file name

# LEVEL 3

username: bandit3    password: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

listing files in our current directory

![image](https://github.com/user-attachments/assets/94ddee54-f457-4d94-9f53-0abe8be10aa2)

we found a directory there so we navigated into it. We tried listing files there but it was like there was nothing, we moved on to check for hidden files and as we will have it, we saw something trying to hide from us hehe.

![image](https://github.com/user-attachments/assets/fd89e9d2-a607-4aa2-97ec-f463393605d3)

viewing the file

![image](https://github.com/user-attachments/assets/ed7b0227-3602-4471-a20f-71028bb56c82)

# LEVEL 4

username: bandit4     password:  2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

listing files in our current working directory, we found a dir, inhere. We navigated into it and found a number of files. 

![image](https://github.com/user-attachments/assets/f8b1faee-6fb5-4892-9cab-14b5bc36b600)

For ease, we use the <file> command to view what type of files they are. I tried to use wildcard but it gave error. 

![image](https://github.com/user-attachments/assets/c54a9c99-9543-4b45-8862-6491cd81ea37)

I remembered they are all dash files so i used ./* instead of just * and boom!!!, it came to us.

![image](https://github.com/user-attachments/assets/f73fe092-1154-4434-a502-d3310d4e9756)

To view the file we use normal ```cat``` and then we get the password for the new level.

![image](https://github.com/user-attachments/assets/465be3da-99f8-4cf3-b30b-8703633452cd)

# LEVEL 5

username: bandit5     password: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

After we successfully logged in, we navigated to inhere directory and saw many other directories. To save time and stregnth we use the ```find``` command.

![image](https://github.com/user-attachments/assets/218f2d5b-caa6-4e72-9dca-1f9d927ab472)

Using the ```find``` command with the parameters given already, the search became easy and we found our file...

![image](https://github.com/user-attachments/assets/41c85cf3-ec23-4d04-bd0a-d19034c26083)

# LEVEL 6

username: bandit6   password: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

After we logged in, we tried to list files and we could not find anything not even hidden files. We read the instructions again and they said it was somewhere on the server so we just went ahead to use the ```find``` command.

![image](https://github.com/user-attachments/assets/25564ea1-81b0-404d-96df-16d3a81efd2d)

We narrowed our search with that ```2>/dev/null``` thing and we got a place where the next password is. I copied the path and catted it out.

![image](https://github.com/user-attachments/assets/a8d05a39-6f2c-4554-927b-d91c76ec59c0)

# LEVEL 7

username: bandit7    password: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

We list the contents in our working directory and we see a .txt file, catting it will give one kain long novel so we just used ```grep``` to look for the word. Very easy for us to get the password.

![image](https://github.com/user-attachments/assets/5fdf477d-742e-49ee-89ba-663f3b6c7477)

# LEVEL 8

username: bandit8     password: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

For this level, we were also told that the password is in a file called data.txt. But in this case, almost each line is repeated as shown below using sort command:

![image](https://github.com/user-attachments/assets/fa6f3dbd-d33a-4258-a10e-c9f0c395de70)

As you can see the end of the file are arranged. We will be piping the sort command with ```uniq``` and indicating we want just unique lines using the -u flag which tells it to show only unique lines

![image](https://github.com/user-attachments/assets/44a1f3b4-e731-49b4-8d8a-b4a2c78d7965)

# LEVEL 9

username: bandit9      password: 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

We were given a file that is not an ASCII text. If we try to cat it, we get strings of data and we can't even grep. So we wil use strig command and then ```grep``` '========='

![image](https://github.com/user-attachments/assets/1e17faf7-6f37-4ff5-a19e-c8cf379f7701)

# LEVEL 10

username: bandit10    password: FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

After successfully loggin in, we found a data.txt which was an ascii text. As we catted it, we saw it was an encoded message in base64. We can either use an online tool or we use the ```base64``` command. 

SYNTAX: ```base64 -d "name of file"```. The -d flag is to decode

![image](https://github.com/user-attachments/assets/61802453-66d4-473b-9d9e-974c1fb67bbd)

# LEVEL 11

username: bandit11    password: dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

For this, we were also given a file that contained set of characters we can't pronounce. We realize it is also a cipher text and it was rotated 13 times. We can either do this using ```tr``` command or we use an online tool. I would have preferred not to use terminal but as per this game is supposed to help make us better and more familiar with linux commands, I won't be using the online tool. We can as well do it manually...that one will stress you small sha, just move each character 13 times. 

![image](https://github.com/user-attachments/assets/5700e16e-c65c-4675-b71c-e4e90685707d) 

OR

![image](https://github.com/user-attachments/assets/5b3720ff-c3ad-4dc6-af38-88848687feff)

And boom!, we have our password.

# LEVEL 12

username: bandit12 password: 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

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

username: bandit13     password: FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn 

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

username: bandit14        password: MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS

For this level, we will be able to get the password to the next level by submitting the password we retrieved in the last level to port 30000 on localhost. We can either use local host or use 127.0.0.1 for this, both works. 

![image](https://github.com/user-attachments/assets/5b8b16c7-5264-42c2-bd2f-d2f5d81b91f8)

As you can see, both ways gave same password. We meauve

# LEVEL 15       

username: bandit15              password: 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo

For this level, we will also be submitting the old password to get the password for the next level, this time they gave a different thing.

![image](https://github.com/user-attachments/assets/8dabfa18-1a1f-4745-89c8-68d51f365c55)

I just connected the localhost server woth the openssl clinet and pasted the password from this level since they told us it was using ssl encryption.

# LEVEL 16 

usernmae: bandit16              password: kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

For this level, we need to know which and which ports are opened as they gave us a range so we will be using the ```nmap``` tool. It is known as network mappper, it can do alot of things such as network scanning, OS detection, host discovery etc. The syntax for this is ```nmap <ip address>```. Other flags can be attached depending on what you want to do with the scan. You can use the man page to read more.

![image](https://github.com/user-attachments/assets/3ee896d9-40d4-48ea-b985-f35d2cd77e44)

After running the scan, we were gicen a number of opened ports but we don't know what service we are running on so we add the -sV flag for it to give us that. Reason for this is so we can know theport that has a listener on it.

![image](https://github.com/user-attachments/assets/f51e0991-2e08-4460-aa83-7a34386ae5a3)

We have 5 ports running here, our best guess is 31790 so we will try to connect to that using openssl using the same format.

For this we will be using the ```ncat``` command. The syntax is, ```ncat --ssl localhost 31970```

After doing that, we paste the password for this level and then we get a RSA Key. The key can be used to login into the next level whic is bandit 17 just like we did in level 14.

# LEVEL 17 

username: bandit17          password: EReVavePLFHtFlFsjn3hyzMlvSuSAcRD

After successfully logging in, we wil find the password for this level wehre passwords are being stored. 

![image](https://github.com/user-attachments/assets/4cf630e8-e7a6-4159-ac01-8c98d633883e)

Now we were told there are two different passswords, I actually do not know what command to use. They gave a list of commands as usual and there was this one i was unfamiliar with. After a little research, It was what i eventually used. 

After listing the files in our current working directory, we see two different files, when i view both files, I see they look so familiar so i used the ```diff``` command to check for the difference. Our password should be in the ```password.new``` so we look out for that. 

![image](https://github.com/user-attachments/assets/eae64af7-74f2-41ff-a6f7-2ef901bb7a7d)

And boom! we found our password for the next level

# LEVEL 18

username: bandit18     password: x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO

Unfortunatly for us someone modified the .bashrc file to keep logging us out.

![image](https://github.com/user-attachments/assets/a9cf92d5-ca25-48e3-8d72-cc96e8e808e8)

After seeing i won't be able to login, i decided to run command with ssh instead of running it when i am logged in. Since we were told there was a readme file there, we ```ls``` to view the files and the we ```cat``` it after.

![image](https://github.com/user-attachments/assets/2857c77c-60c4-40e7-96ae-d445b3b0ce06)

We now have our password for the next level.

# LEVEL 19

username: bandit19        password: cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8

After successfully logging in, i tried to check the password in the ususal place but it says permission denied. So i followed the instruction given and read a little about setuid. First we need to check which user can run the file that was given, for that we use ```ls -l``` 

![image](https://github.com/user-attachments/assets/13260fea-0f53-48f9-90c2-e4e3b125f6a5)

I then tried to execute the file to see the usage and it gave me one. I followed it and it became clearer, I could run this as bandit20 so it was possible for me to check the password and not get a permission denied.

![image](https://github.com/user-attachments/assets/8dff0a7d-6f66-496d-8310-1e26fe7e2f46)

I did just that and it gave me this

![image](https://github.com/user-attachments/assets/e2afd225-2edb-48da-b1ed-22435dcfcbf3)

# LEVEL 20

username: bandit20           password:  0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO

Reading the level goal, I realized I will be needing netcat to listen and then paste password somehow. I proceeded to opening another tab. I will be listening on one of them and executing the setuid file on the other.

![image](https://github.com/user-attachments/assets/36d121a8-3a0a-4b72-8530-a943acdd9d96)

After multiple trials, it gave me the password for the next level.

![image](https://github.com/user-attachments/assets/49e2e4ed-cbf3-44a0-a286-dd7be962b7fe)

# LEVEL 21

username: bandit21            password: EeoULMCra2q0dSkYj561DX7s1CpBuOBt

After successfully loggging in, we follow the goal that was given to check for cronjobs. We will be checking the ```/etc/cron.d``` to see the program that is running immediately.

![image](https://github.com/user-attachments/assets/b6135cf2-74ea-47ab-beb5-9df93f874b94)

As we can see, we have a file called cronjob_bandit22, we will try to see the content of the file for any hints.

![image](https://github.com/user-attachments/assets/eab7a648-e45e-468e-ba21-ef22c6f07b1f)

We have a bash file running /usr/bin. We will navigate into there and view the conent of the bash file. 

![image](https://github.com/user-attachments/assets/d9bddc59-a02c-4258-89b3-3bbe5e7d699c)

From the bash file, we see that everyone has priviledge to read /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv and the password for the next level is written there. So we will just view the content of this file and hope to see our next password there.

![image](https://github.com/user-attachments/assets/af20cad2-1460-4702-9a5a-db223fcd09b5)

# LEVEL 22             

username: bandit 22            password: tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q








