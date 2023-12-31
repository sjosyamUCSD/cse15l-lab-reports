**PART 1**
`StringServer` code:
![Image](https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/802b1601-1f41-42a2-8f0a-032f45953fbb)

Two screenshots using `/add-message?s=`:
![Image](https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/a647d243-44b5-4aec-beb1-7a096ebd402f)

The handleRequest method was being called. In this method, an if condition checked if the path of the URL contained `/add-message?s=`. The `handleRequest` method takes an argument of a `URI url`. In this first example, the arguments of the url would be /add-message?s=Hello. Although the class, `Handler`, implements URLHandler, there are no other arguments for the class itself. `handleRequest` is a `public String` method, meaning it expects a String value to be returned. 

![Image](https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/4bb6112c-1c11-4c1f-94cd-2e4a1f9c581c)

Although the same method was being called and the same if condition was checked, this method would take in the argument of the URL ending with /add-message?s=How are you as the argument. This time, although a String value is still returned, the newly added string is concatenated with the previous string. This new value, stored in a variable called `everyMessage`, is returned to display the total. Before, the value had changed to the string, "Hello". When the new string value is added, the value changes to "How are you" to list the second element as the output. 

**PART 2:**
1) The path to the private key for your SSH key for logging into `ieng6` (on your computer or on the home directory of the lab computer).

The path to the private key is located in `/Users/sahithijosyam/.ssh/id_rsa`. 

![Image](https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/c32fa93b-bce6-4131-b7a7-b44db3f2e032)
 

2) The path to the public key for your SSH key for logging into `ieng6` (within your account on `ieng6`).

The path to the public key is located in `/Users/sahithijosyam/.ssh/id_rsa.pub`

![Image](https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/817db327-74e9-4fe3-b8c6-6c0254cc79c9)

  
3) A terminal interaction where you log into `ieng6` with your course-specific account without being asked for a password.
   ![Image](https://github.com/sjosyamUCSD/cse15l-lab-reports/assets/146763351/20a66353-6ab8-4ad0-b948-b205f5dcbd5c)

**PART 3:**
Something that I learned from week 2 and week 3 that I did not know before was actually the whole process of running a server on my computer and seeing the relationships between multiple parts. I also learned that public keys can be copied into different files by taking advantage of command lines like mkdir and scp.

