**Installing VScode**
  1. Go to [https://code.visualstudio.com/Download](https://code.visualstudio.com/Download)
  ![Image](VSCode_Download.png)
  2. Install it for your OS
  3. When open it, it should look like this
  ![Image](VScode.png)

**Remotely Connecting**
  1. Find your CSE 15L account (if you don’t know it) with the Account Lookup at [https://sdacs.ucsd.edu/~icc/index.php](https://sdacs.ucsd.edu/~icc/index.php) and you should enter in your UCSD username and PID to find your account 
  ![Image](AL.png) <br>
  
  2. Once you've gotten the username for your account to reset your password, just click on your CSE 15L account username and you should be able to reset your password with this ![Image](password.png) <br>
  3. Launch VScode and open a terminal with
  ```Ctrl or Command + ` ```
  or use the Terminal -> New Terminal menu option
  <br>
  4. After type in “ssh cs15lsp23zz@ieng6.ucsd.edu” and replace the zz with the letters in specific CSE 15L account 
  It should look like this below <br>
      ```console
      $ ssh cs15lsp23zz@ieng6.ucsd.edu
      ```
<br>

  5. After you connect you will get a message that says 
      ```console
      ⤇ ssh cs15lsp23zz@ieng6.ucsd.edu
      The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established. 
      RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
      Are you sure you want to continue connecting (yes/no/[fingerprint])?
      ```
  Make sure to type in **yes** <br>
        <br>
        
        
      ```console
      # On your client
      ⤇ ssh cs15lsp23zz@ieng6.ucsd.edu
      The authenticity of host 'ieng6-202.ucsd.edu (128.54.70.227)' can't be established.
      RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
      Are you sure you want to continue connecting (yes/no/[fingerprint])? 
      Password:  
      ```
  5. After you type in **yes**, a new line that says will appear and you will input the 
     password for your CSE 15
  ```console
  Password:  
  ``` 
  <br> (Note: when type in your password it won’t show any characters moving 
   for security reasons, so you can still type your password in and hit enter) If your password isn’t 
   working then you should try to reset your password and see if that fixes the issue. <br>
      
  6. When you successfully input your password this should show up (below) and now your terminal is connected 
     to a computer in the CSE basement and any commands you run will run on that computer!
     
     ```console
      # Now on remote server
      Last login: Sun Apr  23 14:03:05 2023 from 107-217-10-235.lightspeed.sndgca.sbcglobal.net
      quota: No filesystem specified.
      Hello cs15lsp23zz, you are currently logged into ieng6-203.ucsd.edu

      You are using 0% CPU on this system

      Cluster Status 
      Hostname     Time    #Users  Load  Averages  
      ieng6-201   23:25:01   0  0.08,  0.17,  0.11
      ieng6-202   23:25:01   1  0.09,  0.15,  0.11
      ieng6-203   23:25:01   1  0.08,  0.15,  0.11

      Mon Apr 24, 2023 11:28am - Prepping cs15lsp23
      ```

  
 **Trying Some Commands!** <br>
 
  Since you’re connected you can now try out some commands <br>
  Here are some specific useful commands to try: <br>
* ```cd ~``` changes the current working directory to the user's home directory <br>
* ```cd``` allows you to move between directories <br>
* ```ls -lat``` lists the files and directories in the current working directory in a long format <br>
* ```ls -a``` lists all files and directories, including hidden ones, in the current working directory <br>
* ```ls <directory>``` where ```<directory>``` is ```/home/linux/ieng6/cs15lsp23/cs15lsp23abc```, where the ```abc``` is one of the other group members’ username <br>
* ```cp /home/linux/ieng6/cs15lsp23/public/hello.txt ~/``` copies the file "hello.txt" from the directory to the user's home directory <br>
* ```cat /home/linux/ieng6/cs15lsp23/public/hello.txt``` displays the contents of the file "hello.txt" located in the directory <br>
  
  Here is an example of some of the commands being ran
  ![Image](Testing.png) <br>
  
  In this example I first ran ```ls -lat``` <br>
  
  ```console
  [cs15lsp23fw@ieng6-202]:~:18$ ls -lat
  ```
  <br> 
  which resulted in 
  ```console
  total 116
  -rw-r--r--   1 cs15lsp23fw ieng6_cs15lsp23  1337 Apr  6 10:55 .modulesbegenv
  -rw-------   1 cs15lsp23fw ieng6_cs15lsp23     0 Apr  6 10:55 .bash_history
  drwxr-s---   6 cs15lsp23fw ieng6_cs15lsp23   718 Apr  6 10:47 .
  -rw-r-----   1 cs15lsp23fw ieng6_cs15lsp23  4096 Apr  6 10:40 .motd
  drwxr-sr-x   2 cs15lsp23fw ieng6_cs15lsp23  4096 Apr  6 10:40 perl5
  drwxr-sr-x   3 cs15lsp23fw ieng6_cs15lsp23  4096 Apr  6 10:40 .local
  drwxr-sr-x   3 cs15lsp23fw ieng6_cs15lsp23  4096 Apr  6 10:40 .config
  drwxr-sr-x 506 cs15lsp23   ieng6_cs15lsp23 40960 Apr  6 10:40 cache
  drwxr-sr-x   1 cs15lsp23fw ieng6_cs15lsp23  4096 Apr  6 09:55 ..
  -rwxr-x---   1 cs15lsp23fw ieng6_cs15lsp23  4096 Apr  5 17:10 .zshrc
  -rwxr-x---   1 cs15lsp23fw ieng6_cs15lsp23  4096 Apr  5 17:10 .zshenv
  -rwxr-x---   1 cs15lsp23fw ieng6_cs15lsp23  4096 Apr  5 17:10 .zprofile
  -rwxr-x---   1 cs15lsp23fw ieng6_cs15lsp23   290 Apr  5 17:10 .profile
  -rwxr-x---   1 cs15lsp23fw ieng6_cs15lsp23   481 Apr  5 17:10 .procmailrc
  -rwxr-x---   1 cs15lsp23fw ieng6_cs15lsp23  1931 Apr  5 17:10 .login
  -rwxr-x---   1 cs15lsp23fw ieng6_cs15lsp23  1961 Apr  5 17:10 .locallogin
  -rwxr-x---   1 cs15lsp23fw ieng6_cs15lsp23   837 Apr  5 17:10 .kshrc
  -rwxr-x---   1 cs15lsp23fw ieng6_cs15lsp23   431 Apr  5 17:10 .cshrc
  -rwxr-x---   1 cs15lsp23fw ieng6_cs15lsp23   155 Apr  5 17:10 .bashrc
  -rwxr-x---   1 cs15lsp23fw ieng6_cs15lsp23  1692 Apr  5 17:10 .bash_profile
  ```
  <br> 
  What ```ls -lat``` does is lists the files and directories in the current working directory in a long format, sorted by modification time, with the most recently modified files or directories appearing first.
  
  After I ran ```ls -a```
  
  ```console
  [cs15lsp23fw@ieng6-202]:~:19$ ls -a
  ```
  <br> which listed all the files and directories, including the hidden ones, in the current working directory.
  
  ```console
  .bash_profile .config	 .local	         .modulesbegenv   .profile    .zshrc
  .bashrc	      .cshrc	 .locallogin     .motd		  .zprofile   perl5
  .cache 	      .kshrc     .login          .promailrc       .zshenv
  ```
  <br>
  
  Another thing I did was create a new directory called "hello" with the command ```mkdir -v hello```  ,then I switched to the "hello" directory with ```cd hello``` and lastly I printed the absolute path of the working directory with ```pwd``` which resulted in ```/home/linux/ieng6/cs15lsp23/cs15lsp23fw/hello``` <br>
  ```console
    [cs15lsp23fw@ieng6-202]:~:20$ mkdir -v hello
    mkdir: created directory ‘hello’
    [cs15lsp23fw@ieng6-202]:~:21$ cd hello
    [cs15lsp23fw@ieng6-202]:hello:22$ pwd
    /home/linux/ieng6/cs15lsp23/cs15lsp23fw/hello
    ```
Overall, I learned useful commands for the terminal to help my access and look for certain directories, files, etc.
  
  
  
  
  
  
  
  
  
 
  
  
  
     
