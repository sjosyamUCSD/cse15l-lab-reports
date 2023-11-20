**Logging into ieng6**
To log into ieng6, I typed `ssh cs15lfa23ic@ieng6.ucsd.edu` then <enter> to execute. 
![Image]("https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/c370cfb9-4468-4a01-ba7b-70c63cfeceb2")

**Cloning fork of the repository using the SSH URL**
To do this, I typed `git clone git@github.com:sjosyamUCSD/lab7.git` then <enter> to execute. 
![Image]("https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/166bbf81-9589-4bd3-a5e6-def64f358c2c")

**Running the tests and demonstrating that they fail**
Here, I typed `cd lab7<enter>` followed by `bash test.sh<enter>`

![Image]("https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/369f6782-f9e1-45c3-a7ba-61c5f82167db")

**Editing the code file to fix the failing test**
After typing `vim ListExamples.java<enter>`, I was led to the following:

![Image]("https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/41930976-8544-4679-a22a-6b3456cb1559")

To fix the code, I typed `<shift+g>` to jump to the bottom and went to the line to be fixed by using `<up><up><up><up><up><up>`.
Then, I used <shift+e> to jump to the character, `<i>` to enter insert mode, then `<right><backspace><2><esc>`, to change the index accordingly.
Finally, I typed `<:wq><enter>` to save and exit out. 

![image]("https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/ed10aa24-5f0b-4f7b-aabe-0ba4aaa46f9c")

**Re-running the tests to demonstrate that they work**
By pressing `<up><up><enter>` to run the command that was two up in my history, I was able to rerun the tests and show that they now work. 

![image]("https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/c0806421-9b44-455d-aa50-35b6a8454013")

**Committing and pushing the changes**
By typing `git add ListExamples.java<enter>` and `git commit -m "successful run"<enter>` I was able to commit and add a message.
Then, I pushed the change onto Github by typing `git push<enter>`. This is shown in the image below. 

![image]("https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/4d4cd9fb-0782-45df-8152-93c5a22b827a")


