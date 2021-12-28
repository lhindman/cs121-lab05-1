# Module 5 Lab Guide (part 1)
## Getting Started
[Lab Introduction Video](https://youtu.be/4m5AwuwMg6E)  

### Code Style Requirements
Please review the [CS121 Style Guide](https://docs.google.com/document/d/1LWbGQBKkApnNAzzgwOSvRM03DmhYWx5yEfecT2WXfjI/edit?usp=sharing) and apply it in all lab activities and projects this semester. Coding Style will assessed as part of your lab and project grades.

### Code Quality Requirements
- Code must compile without warnings using openjdk11
- Code must run without errors or warnings on safe-path and edge test cases
- More to come as we learn about input validation and exception handling

## Lab Warmup - QuickPick (Required)
### Problem Description

Write a program that will randomly generate lottery ticket numbers. You code will generate five numbers in the range of 1 through 69 and a single power pick number in the range of 1 through 26. The numbers will be generated randomly WITH replacement, meaning that the same number can appear multiple times on the ticket. When printed to the console, each number should be zero-padded to two places and separate from each other with hyphens. The power pick number should be zero-padded to two places separated from the first five numbers with spaces and a forward slash. In addition, your program should prompt the user for their name and for a seed value to initialize the Random object so that the ticket numbers are reproducible.

#### Expected Program Output (with sample user input)
```
Please enter your name: Luke
Please enter a seed value: 123

Hello Luke,
Your quick pick is: XX-XX-XX-XX-XX / XX
```

#### Expected Program Output (with sample user input)
```
Please enter your name: Luke
Please enter a seed value: 76281564

Hello Luke,
Your quick pick is: XX-XX-XX-XX-XX / XX
```

### Program Design
While it is possible to implement this entire program in the main() method, it is a good practice to organize related sections of code into separate methods making the overall code easier to read and to allow code to be reused more easily. The main() method will implemented in a class called QuickPick. The following static methods should be implemented in a seperate call called LabUtility. Use the javadoc comments below to implement the expected functionality of each static method.

```
public static String getName(Scanner kbd) {...}
```

```
public static long getSeed(Scanner kbd) {...}
```

```
public static void generateTicket(Random rnd) {...}
```

### Implementation Guide
1. Expand the folder named QuickPick and open both QuickPick.java and LabUtility.java
2. Design a program to satisfy the requirements in the Problem Description and Program Design sections
3. Test the program using the sample user input and compare against the expected output. Carefully think about each of the different cases you'll need to test for to verify that the application is functioning properly.
4. Commit the changes to your local repository with a message stating that Lab Warmup is completed.
5. Push the changes from your local repository to the github classroom repository.

## Lab Activity 1 - HousingCrunch (Required)
### Problem Description

By now most folks are aware of the housing crisis in Boise, Idaho. Even decisions as to whether to buy a house or an apartment have become difficult. To help address this issue, write a program that help folks make this decision. This program will prompt the user for their name and a seed value (for reproducibility), then display advice on whether they should purchase a **Mansion**, **Apartment**, **Shack** or **House**.  :) 

#### Expected Program Output (with sample user input)
```
Please enter your name: Luke
Please enter a seed value: 123

Hello Luke,
You should buy a XXXXXXXXX
```

#### Expected Program Output (with sample user input)
```
Please enter your name: Luke
Please enter a seed value: 9853482

Hello Luke,
You should buy a XXXXXXXXX
```

### Program Design
Please copy LabUtility.java from the Lab Warmup into the HousingCrunch folder.  This will allow reuse of both the getName() and getSeed() static methods.  

Please add a main() method to the class in HousingCrunch.java.  Declare and instantiate an ArrayList of Strings named homeList and add each of the following options to the list in the order as shown below:
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

## Coding Journal (Optional)
Keep a journal of your activities as you work on this lab. Many of the best engineers that I have worked with professionally have kept some sort of engineering journal. I personally packed notebooks around with me for nearly 8 years before I began keeping my notes electronically.   

Your journal can track ideas, bugs, cool links, code snippets, shell commands, rants, or simply a reflection on what worked well or not-so-well with this lab activity. I will not be grading the content of your journal, but I will expect at least two timestamped journal entries of at least a 75 to 150 words each added to the provided Journal.md file.  The purpose of this component is to help develop the habit of taking notes and creating documentation while you code. The more detail you provide the better as that will help you if you ever need to refer back to this project in the future.

## Markdown Resources
Markdown is a notation that is used to format text documents.  It is widely used in Software Development shops around the world, which is why we're asking you to use it in your lab documentation.  

Github provides a guide for getting started:  [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
