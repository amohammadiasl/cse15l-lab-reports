# Lab report 4
### Step 1: Log into ieng6
#### SSH into my username
I typed in "ssh" and then typed my username "cs15lfa23ay@ieng6.ucsd.edu" and finally pressed `<enter>` to log onto ieng6. <br>
<br>
![image](IMG1.png) 
<br>
I was prompted to enter my passowrd although I already have my save key (I am guessing this is because I was on my home connection. I had the same issues at UCSD until I logged into UCSD_Protected). I typed in "*******" then pressed `<enter>` and got logged in. <br>
<br>
![Image](IMG2.png) 
<br>
### Step 2: Clone the fork using the `SSH` link <br>
![image](IMG3.png) 
<br>
I copied the `SSH` URL from my forked repo on Github, using `<Ctrl>` `c`, and the typed `git clone` into the terminal and pasted the URL with `<Ctrl>` `v` and finally pressed `<enter>` to clone the repository.
<br>
<br>
![Image](IMG4.png)
<br>
I then typed `cd` and `lab7` and pressed `<enter>` to change into the lab7 directory.
<br>
### Step 3: Run the tests to demonstrate they fail
In this step, I typed in `ls` and pressed `<enter>` to display the files in the current directory. This is because majority of the time, we will not remeber the name of a file of the top of our head, so it is very useful to `ls` into a directory and see its contents. Once I found the file that I needed (test.sh), I typed `bash<space>test.sh` and pressed `<enter>` to run the tests within the bash file. The reason I typed `bash` is because `test.sh` essentially is a shortcut to run the java file `ListExamplestests` which has a series of `junit` tests, written to test the correctness of `ListExamples`. <br>
<br>
![Image](IMG5A.png)
<br>
As displayed in the image above, there is 1 failure after running the 2 tests. 
### Step 4: Edit the code to fix the failing test
To edit the code, I used the built-in text editor, Vim. I typed `Vim ListExamples.java` into the terminal then pressed `<enter>`.
<br> <br>
![Image](IMG6.png)
<br> <br>
This is the terminal after I pressed `<enter>`.
<br> <br>
![image](IMG7.png)
<br><br>
Now, we have to remember, the error in the code is just that `index1` is used instead of `index2` in the final loop in `merge`. So what I am going to do is to search for the word `index1` and skip through until I find the correct one. <br>
**How? :** I press `ESC` to make sure that I am in normal mode, then I press `/` and then I type `index1`. As we learned in class, `/<text>` searches for a keyword. The forward-slash is basically the search command and the text after it is the keyword that it will look for. We also should not forget to press `<enter>` to lock in our word, `index1`. 
<br><br>
![image](IMG8.png) 
<br><br>
As we see in the image, it found the first occurrence of `index1`. Now, that specific occurrence of `index1` is not the one we are particularly looking for. But nothing to worry as we can press `n` to go to the next occurrence of `index1`.  
<br><br>
![image](IMG9.png)
<br><br>
![image](IMG10.png)
<br><br>
After pressing `n` 9 times, we are on the desired occurrence of `index1`. So far, what he have in this step if `vim ListExamples.java <enter> / i n d e x 1 <enter> n n n n n n n n n` (I separated them by a space to make it easier to read). Now that we are at the desired word, we need to edit the 1 and turn it into a 2. <br>
Notice that currently, we are on the "i" of `index1`and we need to relocate our cursor to the 1. We learned in clas that we can use `h`,`j`,`k`, and `l` to move around in vim. I used `l` because it moves the cursor to the right by 1 each press. I pressed `l` 5 times to get to 1. So far we have `vim ListExamples.java <enter> / i n d e x 1 <enter> n n n n n n n n n l l l l l`.
<br><br>
![image](IMG11.png)
<br><br>
Now to delete the 1, I pressed `x`. We learned in class that `x` deletes whatever character the cursor is on.
<br><br>
![image](IMG12.png)
<br><br> 
Now that the 1 is deleted, I pressed `i` to go into insert mode.
![image](IMG13.png)
