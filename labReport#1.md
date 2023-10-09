1) **cd commands with no arguments, with path to directory and with path to file as arguments:**

![Image](https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/2c486e2d-bd1b-4c46-938f-dfb6fae3a1ee)

*Explanation:*
* The cd command with no arguments does not generate any output. This is because the cd command is to change between directories. With no argument, a directory is not found to change to. Similarly, a file cannot be given to the cd command as the command can only swtich between one directory to another, and therefore is an error. 

  
2) **ls commands with no arguments, with path to directory, and with path to file as arguments:**
   ![Image](https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/ec8f2fbb-4701-42b7-a963-c7e5517a748f)
   
*Explanation:*
* The ls command with no arguments provides only the output "lecture1" as this command is to list out the files in the current directory. With the path to a directory, the command line outputs all the files that are within "lecture1". Lastly, with the path to file as an argument, because the command line is used to list out the files, it is called upon itself and outputs the same argument that was entered as seen. This is not an error. 
  
 3) **cat command with no arguments produces:**
   ![Image](https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/00c4e9f6-fc2a-4c09-bfec-1d7cc703314b)

  **cat command with path to directory and command with path to file as an argument:**
  ![Image](https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/30c4a8a1-5793-4177-9f8f-14ee136c9e4a)


*Explanation:*
* The cat command is used to print out the contents of the given argument. While not providing any arguments, the terminal waits for further input. While the argument is a path to a directory, the command line outputs the fact that it is simply a directory with no further file to provide contents of. Lastly, with the argument as a path to file, the command line is able to read and print out contents of the file given as seen with both the fr.txt file as well as the Hello.java file. This is not an error.


