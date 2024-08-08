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

# LEVEL 13

username: bandit13        password: FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn






