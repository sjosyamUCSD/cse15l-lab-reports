**PART 1 - DEBUGGING SCENARIO**
Student post: 
Hi, I had a problem with my grade.sh bash script as it is marking the java files inputted as completely correct although there are errors in the file after I have git cloned a student repository to be graded. Below is a screenshot I have attached to show this problem. The screenshots show my bash script and terminal output. 
Could I get help with this? 

Bash Script: 
![Symptom](https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/469aaa38-9bae-4d38-a616-9daa913636eb)

Terminal:
![TerminalOutput](https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/f11ba81b-b1e6-48c7-a63c-94d4d7dfb9d1)

TA Response: 
Thank you for your question. Try investigating what the first and second if conditions in your bash script is checking for. 

*Student*: 
It seems like the first if condition is checking for if the student submissions file exists. The second if condition essentially checks if the submitted files are correct. I moved the line of code previously at line 20 to be within the second if condition to grade the files only after it is checked if they exist. I also added an else statement to the second condition for when the files fail as I realized I previously lacked this. This also seemed to fix the problem I was having before as it is properly returning that the tests have failed. 

![fixed](https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/a25fe0a3-a1e2-487b-95ab-23a8d311d551)

*TA*:
Good job. What exactly seemed to be the issue?

*Student*: 
I believe it may have been that line 20 was actually checking if the java files were being properly compiled and run, checking the correctness of line 19 rather than grading the contents of the file itself. By moving it to be within the second if condition, this issue was resolved. By simply changing this and running `bash grade.sh https://github.com/ucsd-cse15l-f22/list-methods-lab3`, proper results were shown. 

**PART 2- REFLECTION**
  Something that I learned from the second half of the quarter that I did not previously know before was Vim.
  During the second half of the quarter, I learned through lecture examples and lab session how to use it and why it would be useful. 
  Since then, it has been something that I took away and used even in personal projects to make the entire process faster. 
  
