This challenge is basically to test knowledge of linux commands. I will try as much as possible to make it short and understandable.

PS: As i solve the challenges, I add.

# LEVEL 0

For this level, we login with the credentials given.

username: bandit0    password: bandit0  host: bandit.labs.overthewire.org  port: 2220

![image](https://github.com/user-attachments/assets/7123ddaa-cde1-4035-81a9-d3004c44160f)

We use the command <ls> to view files and we found a readme file. Viewing it gave us our password. 

![image](https://github.com/user-attachments/assets/0b39b94d-0e10-40b4-89e6-f5ac1eeb1eff)

# LEVEL 1

Credentials...

Username:bandit1  password:ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

After successfully logging in we saw a '-' file and we are not able to cat it. After little reasearch we found out that to cat a dah file you need to add './'

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

To view the file we use normal cat and then we get the password for the new level.

![image](https://github.com/user-attachments/assets/465be3da-99f8-4cf3-b30b-8703633452cd)

# LEVEL 5

username: bandit5     password: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

After we successfully logged in, we navigated to inhere directory and saw many other directories. To save time and stregnth we use the find command.

![image](https://github.com/user-attachments/assets/218f2d5b-caa6-4e72-9dca-1f9d927ab472)

Using the find command with the parameters given already, the search became easy and we found our file...

![image](https://github.com/user-attachments/assets/41c85cf3-ec23-4d04-bd0a-d19034c26083)

# LEVEL 6

username: bandit6   password: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

After we logged in, we tried to list files and we could not find anything not even hidden files. We read the instructions again and they said it was somewhere on the server so we just went ahead to use the find command.

![image](https://github.com/user-attachments/assets/25564ea1-81b0-404d-96df-16d3a81efd2d)

We narrowed our search with that devnull thing and we got a place where the next password is. I copied the path and catted it out.

![image](https://github.com/user-attachments/assets/a8d05a39-6f2c-4554-927b-d91c76ec59c0)

# LEVEL 7

username: bandit7    password: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

We list the contents in our workinf directory and we see a .txt file, catting it will give one kain long novel so we just used grep to look for the word. Very easy for us to get the password.

![image](https://github.com/user-attachments/assets/5fdf477d-742e-49ee-89ba-663f3b6c7477)





