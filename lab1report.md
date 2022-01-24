
# This is the lab report for lab 1
  ![_108857562_mediaitem108857561](https://user-images.githubusercontent.com/33038975/149267061-470b4177-1b10-488f-847a-2317f1be764e.jpg)

  link to homepage: [title](https://yangwestyyy21.github.io/cse15l-lab-reports/index.html)
  
## Part 1:

Here's some screenshots from lab 1 part 2

![Screenshot 2022-01-12 203308](https://user-images.githubusercontent.com/33038975/149266839-4e656872-cb66-41bd-b93b-338780c68c66.png)

![Screenshot 2022-01-12 203238](https://user-images.githubusercontent.com/33038975/149266813-3e53f530-949d-4bc1-953a-ebdaade15353.png)

## Part 2: 

Vscode was already installed on my computer but it's not hard to do. You just need to install it from their site then install a few coding languages. For a Windows computer like me, you also have to change several environment variables for the languages you got. In my case it was Java and JUnit. Here's how it looks like below after getting set up. 
![Screenshot 2022-01-14 200054](https://user-images.githubusercontent.com/33038975/149608040-a15c86fe-9b04-4bcd-83bf-eb38ad6074ad.png)

## Part 3: 

To remotely connect, you have to first find your corresponding account and reset you password. Then, you go on the terminal and type in ```ssh _repository name_``` and enter the passcode to sign in. 

## Part 4: 

The commands in the SSH terminal are the same as the commands on your normal computer terminal. I tried out the ```ls``` command, ```cd``` into a folder I made, and also ```ls -all```, and the other commands should work normally as well, except you're running them remotely on a different computer. There's an example of me running the command below.

![sshtrycommand](https://user-images.githubusercontent.com/33038975/149608279-52d3d5af-e58a-4143-9b4d-a93c9aa7a7bd.png)

## Part 5:

To move files with ```scp``` you first create the file and write what you want with it. Then, you make sure you're on your computer's directory, if you're in the ssh already it will fail (as pictured below). Then you type in ```scp _filename_ _repository name_``` and it will prompt you for the password and you can copy it in. In the picture below it shows me copying some file to the directory. 

![scptossh](https://user-images.githubusercontent.com/33038975/149608498-d079e853-4622-4bb4-ae63-1c0eb2260b71.png)

## Part 6: 

The SSH key makes signing into the ssh directory much easier and faster, no more typing in the password every time. For a windows computer you first make a ssh key using the ```ssh-keygen``` command to make a fancy key box (pictured below). Then you should follow the steps on this site since there's a lot of things to do to setup on a Windows computer  [Microsoft website link](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_keymanagement#user-key-generation). You then save the key to your computer so it will automatically log in for you in the future.

![sshkeything](https://user-images.githubusercontent.com/33038975/149608717-62311c0e-5bb7-4579-93b3-e30b43935a7f.png)


## Part 7: 

To optimize the speed of which you transfer files and log into the ssh directory, there's many things you can do. The easiest is to copy paste and use keyboard shortcuts like the up key on the terminal. You can also use quotes to run multiple commands inside the ssh or use ';' to separate several different commands on one line. You can also put commands you want to run after a ```ssh``` command in a format like ```ssh repository "insert commands"``` to go into the ssh repository and run the commands on the same line. You can sava changes first with a ```scp``` command then use a ; to separate it from a ```ssh``` command into the directory, followed by the ```javac filename``` and running the file. (following screenshot shows how to do it in one line though I ran it without having the WhereAmI.java file open)

![Screenshot 2022-01-24 110117](https://user-images.githubusercontent.com/33038975/150846981-8acd6288-31e3-42eb-bd33-2b1cae39b7ae.png)

