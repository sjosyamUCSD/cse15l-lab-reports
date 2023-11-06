**PART 1- BUGS**
  For this section of the lab report, I decided to choose the `reverseInPlace()` method bug from week 4.

1. A failure-inducing input as a JUnit test
```
public class ArrayTests {
  @Test
  public void testReverseInPlace() {
    int[] input1 = {1,2,3};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{3,2,1},input1);
    }
}
```
   
2. An input that does not induce a failure
```
public class ArrayTests {
  @Test
  public void testReverseInPlace() {
    int[] input1 = {1};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{1},input1);
    }
}
```
   
3. Screenshots of the symptom as the output of running the tests for each input above. 

Here is a screenshot showing the non-failure inducing input: 

Here is a screenshot showing the failure inducing input: 





**PART 2- RESEARCHING COMMANDS**
  For this section of the lab report, I decided to research the `find` command line. 
  The following are 4 find command-line options: 
  1. `-print`: this command-line option prints the path of each of the files that were found to the standard output.
Example #1:

**command:**

     ```
       Sahithis-MBP-2:lab5 sahithijosyam$ find technical/government -print
     ```
     
**output:**

     ```
       technical/government
       technical/government/About_LSC
       technical/government/About_LSC/LegalServCorp_v_VelazquezSyllabus.txt
       technical/government/About_LSC/Progress_report.txt
       technical/government/About_LSC/Strategic_report.txt
       technical/government/About_LSC/Comments_on_semiannual.txt
       technical/government/About_LSC/Special_report_to_congress.txt
       technical/government/About_LSC/CONFIG_STANDARDS.txt
     ```

  
  Example #2:
  
  **command:**
  
       ```
        Sahithis-MBP-2:lab5 sahithijosyam$ find technical/911report -print
       ```
       
  **output:**
  
      ```
        technical/911report
        technical/911report/chapter-13.4.txt
        technical/911report/chapter-13.5.txt
        technical/911report/chapter-13.1.txt
        technical/911report/chapter-13.2.txt
        technical/911report/chapter-13.3.txt
        technical/911report/chapter-3.txt
        technical/911report/chapter-2.txt
        technical/911report/chapter-1.txt
        technical/911report/chapter-5.txt
        technical/911report/chapter-6.txt
        technical/911report/chapter-7.txt
        technical/911report/chapter-9.txt
       ```

    In this command-line option, what is being done is the `find` command line also prints out all of the paths to the files that are returned. 
    This could be useful in situations wherein some form of verification is required. It can be used to double check that the correct files are
    being located from the correct directories rather than simply outputting every file. 
     
  2. `-type type`: this command-line option searches for files of a specific type.
Example #1:

**command:**

     ```
     Sahithis-MBP-2:lab5 sahithijosyam$ find technical/ -type d
     ```
     
**output:**

     ```
     technical/
     technical//government
     technical//government/About_LSC
     technical//government/Env_Prot_Agen
     technical//government/Alcohol_Problems
     technical//government/Gen_Account_Office
     technical//government/Post_Rate_Comm
     technical//government/Media
     technical//plos
     technical//biomed
     technical//911report
     ```

Example #2: 

**command:**

```
Sahithis-MBP-2:lab5 sahithijosyam$ find technical/911report -type f
```

**output:**

```
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-3.txt
technical/911report/chapter-2.txt
technical/911report/chapter-1.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-9.txt
technical/911report/chapter-8.txt
technical/911report/preface.txt
technical/911report/chapter-12.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
```

What is being done here is the individual using this command can clarify specifically what files they are looking for when using the 
`find` command line. This is especially useful in situations where a directory contains a large number of files and only one or, of 
a specific type, are needed to be located. 

  3. `-prune`: this command-line option prevents the find command from searching within the specificied directories.
Example 1:

**command:**

```
Sahithis-MBP-2:lab5 sahithijosyam$ find technical/ -path technical/biomed -prune -o -type d -print
```

**output:**

```
technical/
technical//government
technical//government/About_LSC
technical//government/Env_Prot_Agen
technical//government/Alcohol_Problems
technical//government/Gen_Account_Office
technical//government/Post_Rate_Comm
technical//government/Media
technical//plos
technical//biomed
technical//911report
```

Example 2: 

**command:**

```
Sahithis-MBP-2:lab5 sahithijosyam$ find technical/  -path technical/government -prune -o -type d -print
```

**output:**

```
technical/
technical//government
technical//government/About_LSC
technical//government/Env_Prot_Agen
technical//government/Alcohol_Problems
technical//government/Gen_Account_Office
technical//government/Post_Rate_Comm
technical//government/Media
technical//plos
technical//biomed
technical//911report
```

This command line option is especially useful when an individual needs to find files that are located directly within one directory.
It can be incredibly beneficial to use this where specific directories want to be excluded and the individual wants to skip sections 
of the directory tree. 


4. `-atime n`: this command-line option searches for files that were accessed at the spcecified argument number of days ago, `n`.

Example 1: 
     
**command:**
```
Sahithis-MBP-2:lab5 sahithijosyam$ find technical/ -atime -5
```

**output:**

```
technical//government/About_LSC/Progress_report.txt
technical//government/About_LSC/Strategic_report.txt
technical//government/About_LSC/Special_report_to_congress.txt
technical//government/About_LSC/commission_report.txt
technical//government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt
technical//government/About_LSC/State_Planning_Report.txt
technical//government/Env_Prot_Agen/multi102902.txt
technical//government/Env_Prot_Agen/section-by-section_summary.txt
technical//government/Env_Prot_Agen/jeffordslieberm.txt
technical//government/Env_Prot_Agen/final.txt
technical//government/Env_Prot_Agen/ctf7-10.txt
technical//government/Env_Prot_Agen/ctf1-6.txt
technical//government/Env_Prot_Agen/ctm4-10.txt
technical//government/Env_Prot_Agen/atx1-6.txt
```

Example 2: 

**command:**

```
Sahithis-MBP-2:lab5 sahithijosyam$ find technical/911report -atime -5
```

**output:**

```
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-3.txt
technical/911report/chapter-2.txt
technical/911report/chapter-1.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-9.txt
technical/911report/chapter-8.txt
technical/911report/chapter-12.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
```

This command line can be beneficial when trying to access only recent files in a directory that contain files from any date or time period. 
What the command line does is only find and print out the files from the specified directory within the specified time interval argument, n, 
stated in days. 
