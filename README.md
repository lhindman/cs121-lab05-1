![CS121 Banner](images/CS121-BANNER.svg)
# Module 5 Lab Guide (part 1)
[Lab Introduction Video](https://boisestate.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=212f226d-e5a1-421e-852b-ae2801867bba&start=0)  

**NOTE: Please remember to [open the workspace](images/open-lab-workspace.png) before beginning on the lab activities** 

### Code Style Requirements
Please review the [CS121 Style Guide](https://docs.google.com/document/d/1LWbGQBKkApnNAzzgwOSvRM03DmhYWx5yEfecT2WXfjI/edit?usp=sharing) and apply it in all lab activities and projects this semester. Coding Style will assessed as part of your lab and project grades.

### Code Quality Requirements
- Code must compile without warnings using openjdk11
- Code must run without errors or warnings on safe-path and edge test cases
- More to come as we learn about input validation and exception handling

## Lab Warmup - QuickPick
[Walkthrough Video](https://boisestate.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=3667f5db-0c88-495e-8e49-ae2801867bcc&start=0)
### Problem Description

Write a program that will randomly generate lottery ticket numbers. You code will generate five numbers in the range of 1 through 69 and a single power pick number in the range of 1 through 26. The numbers will be generated randomly WITH replacement, meaning that the same number can appear multiple times on the ticket. When printed to the console, each number should be zero-padded to two places and separated from each other with hyphens. The power pick number should be zero-padded to two places and separated from the first five numbers with spaces and a forward slash. In addition, your program should prompt the user for their name and for a seed value to initialize the Random object so that the ticket numbers are reproducible.

#### Expected Program Output (with sample user input)
```
Please enter your name: Luke
Please enter a seed value: 123

Hello Luke,
Your quick pick is: 48-12-15-36-64 / 08
```

#### Expected Program Output (with sample user input)
```
Please enter your name: Luke
Please enter a seed value: 76281564

Hello Luke,
Your quick pick is: 66-04-27-56-24 / 10
```

The example below shows the expected error handling behavior when invalid seed values are entered.  
#### Expected Program Output (with sample user input)
```
Please enter your name: Luke
Please enter a seed value: bob
Error: Please enter only whole numbers

Please enter a seed value: 12.3
Error: Please enter only whole numbers

Please enter a seed value: 123

Hello Luke,
Your quick pick is: 48-12-15-36-64 / 08
```

### Program Design
While it is possible to implement this entire program in the main() method, it is a good practice to organize related sections of code into separate methods making the overall code easier to read and to allow code to be reused more easily. The main() method will implemented in a class called QuickPick. The following static methods should be implemented in a seperate class called LabUtility. Use the javadoc comments below to implement the expected functionality of each static method.

```
/**
 * Prompt the user to enter their name then use the provided 
 *    Scanner object to read the entire line of user input 
 *    (including spaces) as a String and return this value to
 *    the caller.
 * @param kbd Scanner object bound to System.in
 * @return String containing name
 */
public static String getName(Scanner kbd) {...}
```

```
/**
 * Prompt the user to enter a seed value then user the provided 
 *     Scanner object to read the entire line of user input 
 *     as a String. Use the Long.parseLong() static method to 
 *     convert the String to a long value. If the user enters a 
 *     value that cannot be parsed as a long value, display
 *     an error message and prompt the user to enter the seed value
 *     again. Once a long value has been successfully read, return 
 *     this value to the caller.
 * @param kbd Scanner object bound to System.in
 * @return long value to be used as Random seed
 */
public static long getSeed(Scanner kbd) {...}
```

```
/**
 * Use the provided Random object to generate five integer values in the range
 *     of 1 - 69 (inclusive) followed by one number in the range of 1 - 26 
 *     (inclusive). Print the resulting lottery ticket to the console using
 *     the following format pattern:
 * 
 *     "%02d-%02d-%02d-%02d-%02d / %02d\n"
 * 
 * @param rnd Random object to use for ticket generation
 */
public static void printTicket(Random rnd) {...}
```

### Implementation Guide
1. Expand the folder named QuickPick and open both QuickPick.java and LabUtility.java
2. Design a program to satisfy the requirements in the Problem Description and Program Design sections
3. Test the program using the sample user input and compare against the expected output. Carefully think about each of the different cases you'll need to test for to verify that the application is functioning properly.
4. Commit the changes to your local repository with a message stating that Lab Warmup is completed.
5. Push the changes from your local repository to the github classroom repository.

## Lab Activity 1 - HousingCrunch
### Problem Description

By now most folks are aware of the housing crisis in Boise, Idaho. Even decisions as to whether to buy a house or an apartment have become difficult. To help address this issue, write a program to help folks make this decision. This program will prompt the user for their name and a seed value (for reproducibility), then display advice on whether they should purchase a **Mansion**, **Apartment**, **Shack** or **House**.  :) 

#### Expected Program Output (with sample user input)
```
Please enter your name: Luke
Please enter a seed value: 123

Hello Luke,
You should buy a shack.
```

#### Expected Program Output (with sample user input)
```
Please enter your name: Luke   
Please enter a seed value: 9853482

Hello Luke,
You should buy a apartment.
```

The example below shows the expected error handling behavior when invalid seed values are entered. Notice that you get this error handling behavior for free since it was integrated into the getSeed static method. This is a great example of how methods support code reuse.  
#### Expected Program Output (with sample user input)
```
Please enter your name: Luke
Please enter a seed value: bob
Error: Please enter only whole numbers

Please enter a seed value: 12.3
Error: Please enter only whole numbers

Please enter a seed value: 123

Hello Luke,
You should buy a shack.
```


### Program Design
Please copy LabUtility.java from the Lab Warmup into the HousingCrunch folder.  This will allow reuse of both the getName() and getSeed() static methods.  

In the main() method in the HousingCrunch class, please declare and instantiate an ArrayList of Strings named homeList and add each of the following housing options to the ArrayList in the order as shown below:
- mansion
- apartment
- shack
- house

Use a Random object instantiated using the user provided seed value to randomly select a value from the homeList and display it as a recommendation to the user. The MagicEightBall example from the Deeper Look Lecture Videos is a great reference for randomly selecting items from an ArrayList.


### Implementation Guide
1. Expand the folder named HousingCrunch, copy LabUtility.java from the Lab Warmup and open HousingCrunch.java
2. Design a program to satisfy the requirements in the Problem Description and Program Design sections
3. Test the program using the sample user input and compare against the expected output. Carefully think about each of the different cases you'll need to test for to verify that the application is functioning properly.
4. Commit the changes to your local repository with a message stating that Lab Activity 1 is completed.
5. Push the changes from your local repository to the github classroom repository.
