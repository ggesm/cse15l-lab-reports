**Lab Report 4**

**Step 4: Log into ieng6** <br />
```
Last login: Wed Jun  7 19:17:57 2023 from 108-243-148-249.lightspeed.sndgca.sbcglobal.net
Hello cs15lsp23fw, you are currently logged into ieng6-203.ucsd.edu

You are using 0% CPU on this system
      }

Cluster Status 
Hostname     Time    #Users  Load  Averages  
ieng6-201   19:15:01   11  3.93,  4.08,  3.97
ieng6-202   19:15:01   15  1.92,  0.95,  0.92
ieng6-203   19:15:01   19  0.37,  0.57,  0.52

 
Wed Jun 07, 2023  7:18pm - Prepping cs15lsp23
```

**Step 5: Clone your fork of the repository from your Github account** <br />
```
[cs15lsp23fw@ieng6-203]:~:243$ git clone https://github.com/ucsd-cse15l-s23/lab7
Cloning into 'lab7'...
remote: Enumerating objects: 58, done.
remote: Counting objects: 100% (23/23), done.
remote: Compressing objects: 100% (15/15), done.
remote: Total 58 (delta 8), reused 16 (delta 7), pack-reused 35
Receiving objects: 100% (58/58), 376.84 KiB | 1.80 MiB/s, done.
Resolving deltas: 100% (20/20), done.
```
**Step 6: Run the tests, demonstrating that they fail** <br />
```
[cs15lsp23fw@ieng6-203]:~:244$ cd lab7
[cs15lsp23fw@ieng6-203]:lab7:245$ javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
[cs15lsp23fw@ieng6-203]:lab7:246$ java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
JUnit version 4.13.2
..E
Time: 0.547
There was 1 failure:
1) testMerge2(ListExamplesTests)
org.junit.runners.model.TestTimedOutException: test timed out after 500 milliseconds
        at ListExamples.merge(ListExamples.java:44)
        at ListExamplesTests.testMerge2(ListExamplesTests.java:19)

FAILURES!!!
Tests run: 2,  Failures: 1
``` 
**Step 7: Edit the code file to fix the failing test** <br />
Keys Pressed: To start editting I ran ```vim ListExamples.java```. When I did that I was brought to the first line of the code so I had to go down 43 lines to go to line 44 to edit index1 into index2. ```<down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down>``` Then I had go right 5 times so I could removed the 1 ```<right> <right> <right> <right> <right>```. To remove the 1 I presed ```<x>```. To add the 2 I pressed ```<i>``` then I added the 2 ```<2>```. After that I saved my changes by going to normal mode and typing in ```:wq``` and hitting ```<enter>```

**Step 8: Run the tests, demonstrating that they now succeed** <br />
``` 
[cs15lsp23fw@ieng6-203]:lab7:248$ javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
[cs15lsp23fw@ieng6-203]:lab7:249$ java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
JUnit version 4.13.2
..
Time: 0.018

OK (2 tests)
``` 
**Step 9: Commit and push the resulting change to your Github account** <br />
``` 
[cs15lsp23fw@ieng6-203]:lab7:250$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   ListExamples.java

no changes added to commit (use "git add" and/or "git commit -a")
[cs15lsp23fw@ieng6-203]:lab7:251$ git add ListExamples.java
[cs15lsp23fw@ieng6-203]:lab7:252$ git commit -m "updated"
[main f84241c] updated
 Committer: Giana B Gesmundo <cs15lsp23fw@ieng6-203.ucsd.edu>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 1 insertion(+), 1 deletion(-)
``` 
