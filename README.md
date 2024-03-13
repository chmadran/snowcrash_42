# snowcrash_42


![Screenshot from 2024-03-06 13-58-58](https://github.com/chmadran/snowcrash_42/assets/113340699/1cbffc35-1718-4b96-b5ce-8ecbec074942)

<h2>PREAMBLE</h2>

This project is an introduction to cybersecurity. As a developer, we may have to work on softwares that will be used by hundreds if not thousands of persons. If the software shows some weaknesses, these weaknesses will expose the users through the software.

So we must understand the different techniques used to exploit these weaknesses in order to spot them and avoid them. This project is a modest introduction to the wide world of cyber security. A world where one has no margin for errors.

<h2>HOW IT WORKS</h2>

To make this project, we will have to use a VM with an ISO that has been provided with the subject. If the configuration is right, we will get a simple prompt with an IP and a login request. We can always login with user:levelXX password:levelXX. But this user has limited permissions. 

The goal of every exercice is to find the next level's password, also called token. 

The token can be retrieved with the command `getflag`, but only the user `flagXX` that has elevated permission can get an output when launching the command. So either find a way to retrieve the token, or find a way to login as `flagXX` to launch `getflag`.  

<h2>HOW TO START</h2>

Step by step :
* Create your VM (64 bits), store it in `/sgoinfre`
* Download the iso that's in the subject
* Upon launching your VM for the first time, add the snowcrash.iso image
* You should be prompted to enter a login, enter level00 as login and password
* Good luck !

<h2>USEFUL INFORMATION</h2>

Useful softwares : 
* Ghidra to decompile / analyze binary files, it is already installed on your machine
* John the Ripper / Hashcat to hack passwords  
* Trouver le type d'encodage [ici](https://www.dcode.fr/identification-chiffrement)    

Useful links : 
* [linPEAS](https://github.com/carlospolop/PEASS-ng/tree/master/linPEAS)
* [dirtyCow](https://github.com/firefart/dirtycow/blob/master/dirty.c)

Other stuff : 
* This video [here](https://www.youtube.com/watch?v=Y7KzV-Hl2bw) shows you how to connect in ssh to the snowcrash VM
* I created a VM with an Ubuntu Desktop to test out stuff in parallel / be able to download whatever I wanted [here](https://ubuntu.com/download/desktop)

Project completed with @SERAC-SGM
