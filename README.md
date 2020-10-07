# Lab07 Guide
## Getting Started

Please watch the [Lab07 Walkthough Video](https://www.youtube.com/playlist?list=PLvnIObHoMl8du99YY40zlZ2jtRnYXi21d).

### Code Style Requirements
Please review the [CS253 Style Guide](https://docs.google.com/document/d/1zKIpNfkiPpDHEvbx8XSkZbUEUlpt8rnZjkhCSvM-_3A/edit?usp=sharing) and apply it in all lab warmups, lab activities and projects this semester. Coding Style will assessed as part of your lab and project grades.

### Code Quality Requirements
- Code must compile without warnings using the provided Makefile
- Programs must handle unexpected user input and either reprompt (loops) or gracefully exit with a non-zero exit status.
- Programs must handle error conditions gracefully, without crashing, ideally by checking function returns codes (if available) and returning a non-zero exit status.
- Programs should be free of memory related errors, buffer overflows, stack smashing, etc... Whether the program crashes or not.

## Lab Warmup - Text Analyzer
### Problem Description
<br />
1. Prompt the user to enter a string of their choosing, assuming a 50 character maximum. Output the string. 
<br /><br />

```
Enter a sentence or phrase:
The only thing we have to fear is fear itself.

You entered: The only thing we have to fear is fear itself.

```
<br />
2. Complete the GetNumOfCharacters() function, which returns the number of characters in the user's string. Make sure to count the trailing newline character if applicable. 

*We encourage you to use a for loop in this function.*  

<br />
3. In main(), call the GetNumOfCharacters() function and then output the returned result. 

<br /><br />
4. Implement the OutputWithoutWhitespace() function. OutputWithoutWhitespace() outputs the string's characters except for whitespace (spaces, tabs). Note: A tab is '\t'. Call the OutputWithoutWhitespace() function in main(). 
<br /><br />

```
Enter a sentence or phrase:
The only thing we have to fear is fear itself.

You entered: The only thing we have to fear is fear itself.

Number of characters: 47
String with no whitespace: Theonlythingwehavetofearisfearitself.

```


### Implementation Guide
1. Expand the folder named LabWarmup and open the file named main.c
2. Enter the program code to create an application as described in the Problem Description.
3. Test the program using to ensure it functions as expected.
4. Commit the changes to your local repository with a message stating that LabWarmup is completed.
5. Push the changes from your local repository to the github classroom repository.
6. Update the Coding Journal with an entry describing your experience using the steps outlined below.


## Lab Activity - Authoring Assistant
### Problem Description
<br />
1. Prompt the user to enter a string of their choosing. Store the text in a string. Output the string.  
<br /><br />

```
Enter a sample text:
we'll continue our quest in space.  there will be more shuttle flights and more shuttle crews and,  yes,  more volunteers, more civilians,  more teachers in space.  nothing ends here;  our hopes and our journeys continue!

You entered: we'll continue our quest in space.  there will be more shuttle flights and more shuttle crews and,  yes,  more volunteers, more civilians,  more teachers in space.  nothing ends here;  our hopes and our journeys continue!
```
<br />
2. Implement a PrintMenu() function, which has a string as a parameter, outputs a menu of user options for analyzing/editing the string, and returns the user's entered menu option.  Each option is represented by a single character. 

If an invalid character is entered, continue to prompt for a valid choice. 

*Hint: Implement Quit before implementing other options.*

Call PrintMenu() in the main() function. Continue to call PrintMenu() until the user enters q to Quit. 
<br /><br />

```
MENU
c - Number of non-whitespace characters
w - Number of words
f - Fix capitalization
r - Replace all !'s
s - Shorten spaces
q - Quit

Choose an option:

```
<br />
3. Implement the GetNumOfNonWSCharacters() function. GetNumOfNonWSCharacters() has a constant string as a parameter and returns the number of characters in the string, excluding all whitespace. 

*Hint: Using fgets() to read input will cause your string to have a newline character at the end. The newline character should not be counted by GetNumOfNonWSCharacters().* 

Call GetNumOfNonWSCharacters() in the PrintMenu() function. 
<br />

```
Number of non-whitespace characters: 181
```
<br />
4. Implement the GetNumOfWords() function. GetNumOfWords() has a constant string as a parameter and returns the number of words in the string. 

*Hint: Words end when a space is reached except for the last word in a sentence.* 

Call GetNumOfWords() in the PrintMenu() function.  
<br /><br />

```
Number of words: 35
```
<br />
5. Implement the FixCapitalization() function. FixCapitalization() has a string parameter and updates the string by replacing lowercase letters at the beginning of sentences with uppercase letters. FixCapitalization() DOES NOT output the string. 

Call FixCapitalization() in the PrintMenu() function, and then output the edited string. 
<br /><br />

```
Edited text: We'll continue our quest in space.  There will be more shuttle flights and more shuttle crews and,  yes,  more volunteers, more civilians,  more teachers in space.  Nothing ends here;  our hopes and our journeys continue!
```
<br />
6. Implement the ReplaceExclamation() function. ReplaceExclamation() has a string parameter and updates the string by replacing each '!' character in the string with a '.' character. ReplaceExclamation() DOES NOT output the string. 

Call ReplaceExclamation() in the PrintMenu() function, and then output the edited string. 
<br /><br />

```
Edited text: we'll continue our quest in space.  there will be more shuttle flights and more shuttle crews and,  yes,  more volunteers, more civilians,  more teachers in space.  nothing ends here;  our hopes and our journeys continue.
```
<br />
7. Implement the ShortenSpace() function. ShortenSpace() has a string parameter and updates the string by replacing all sequences of 2 or more spaces with a single space. ShortenSpace() DOES NOT output the string. 

Call ShortenSpace() in the PrintMenu() function, and then output the edited string.
<br /><br />

```
Edited text: we'll continue our quest in space. there will be more shuttle flights and more shuttle crews and, yes, more volunteers, more civilians, more teachers in space. nothing ends here; our hopes and our journeys continue!
```

### Implementation Guide
1. Expand the folder named LabActivity and open the file named main.c
2. Enter the program code to create an application as described in the Problem Description.
3. Test the program using to ensure it functions as expected.
4. Commit the changes to your local repository with a message stating that LabActivity is completed.
5. Push the changes from your local repository to the github classroom repository.
6. Update the Coding Journal with an entry describing your experience using the steps outlined below.

## Coding Journal
Keep a journal of your activities as you work on this lab. Many of the best engineers that I have worked with professionally have kept some sort of engineering journal. I personally packed notebooks around with me for nearly 8 years before I began keeping my notes electronically.   

Your journal can track ideas, bugs, cool links, code snippets, shell commands, rants, or simply a reflection on what worked well or not-so-well with this lab activity. I will not be grading the content of your journal, but I will expect at least two date-stamped journal entries of at least a paragraph each added to the provided Journal.md file.

### Implementation Details
1. Add an entry to the provided Journal.md located in the CodingJournal folder, formatted using markdown notation. You can find a reference at the bottom of this guide.

2. Commit the changes to your local repository with a message stating an entry has been added to the journal.
3. Push the changes from your local repository to the github classroom repository.
4. Repeat for reach additional journal entry
## Markdown Resources
Markdown is a notation that is used to format text documents.  It is widely used in Software Development shops around the world, which is why we're asking you to use it in your lab documentation.  

Github provides a guide for getting started:  [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
