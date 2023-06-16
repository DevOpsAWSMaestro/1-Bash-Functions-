
**Implementing Bash Functions With Colored Output in Continuous Integration Pipelines**


**Lab scenario**

In this lab, you've been hired as a DevOps engineer for a company that is building a new automation department. The organization adopted Continuous Integration pipelines a few months ago and as of now, they have a single script that runs the entire CI pipeline. The new automation team is not happy about the current script's implementation since it doesn't follow proper coding standards and is hard to read and maintain. To tackle the problem, the automation lead has proposed breaking the script down into smaller chunks of code in order to refactor each chunk into a brand new function without affecting the script's behavior. The automation lead has also pointed out that once the script is refactored, they would like to write one more function that implements colored stdout and stderr to better visualize the status of the CI pipeline at any given time. The automation team expects you to implement these changes to improve the overall CI workflow and simplify the current and future development operations.


**Objectives**

1.	Write robust scripts that are easy to read and maintain
2.	Refactor Bash scripts into production-ready functions
3.	Implement CI tests using curl
4.	Transform the Bash stdout with colors
5.	Develop scripts that react to exit signals

**Requirement**

1.	Basic familiarity with Linux
2.	Some experience writing shell scripts
3.	Basic understanding of if conditions and for loops

**What you'll learn**

1.	Bash functions
2.	Loops, traps and conditions
3.	Positional arguments
4.	Colored output with color codes
5.	Advanced usage of the most common Linux commands

**Tasks**

**Task 1**

Explore and test the current CI script before applying any modifications
Before starting to modify the script, you will have to understand the current run_ci.sh implementation. Take your time to go through the run_ci.sh file and ensure that you grasp the steps it's performing. Once you feel a little more familiar, run the file to explore what it does and the output it provides. 
You can run the script in this fashion:  bash run_ci.sh test  to see the "help" displayed to users. You can also try more combinations to see how the script handles different cases.

**Task 2**

Write functions to display "Help" and parse input parameters
In this task, you will focus on the ### Display help to the users and parse parameters. You will have to rewrite the code into two functions. The first function should centralize the help message so that it's not repeated over and over again. Once the function is ready, you can start calling it in the parts of the code where it's needed. The second function should parse the input parameters.
Remember that the behavior of the code MUST NOT change.

**Task 3**

Implement functions to validate tools and generate HTML
In this task, you will work on the ### Required packages and html generation section. You will have to rewrite the code to two more functions. The first function will validate that certain packages are available in the system; these packages are curl and python3. If any of these packages are not found in the system, the script should exit with an error.
The second function should generate a simple HTML file following the current script's approach. 
You can name the functions as you wish and remember that the original script behavior should remain unaltered.


**Task 4**

Write the start_server function
In this task, you will work on the ### Starting the server for CI tests section and you will have to create a function called start_server. The behavior should be exactly the same as the original code but it'll be encapsulated (in a function) to allow for better readability. Once the function is created, you can simply call it  start_server  and it should create the web server.
**
Task 5**

Implement functions to run CI tests
In this task, you will work on the ### Start the CI tests section. There are two existing tests in this script, and you have to move them to different functions. At the end, you will have a function called test_status_code and test_response_body doing only what they need to do (the current script behavior).
Once you write the function, you should create yet another function called run_tests that will call these 2 new functions. This is to improve readability because now you will be able to simply call run_tests  and it will run both of the tests. Remember that the behavior of the script should remain the same.

**Task 6**

Organize the code with groups of functions
In this task, you will work on the ### Clean up  section. You should first create a function that cleans up the HTML and log files generated by the server. It should also kill the web server once the script exits.
Once that is done, you will have successfully rewritten the entire script to functions, and now the only step left is to better organize the code. You have to ensure that all the functions are together in one section, and the calls to the functions should be in another section. Example:
1.	start_server() {...}
2.	run_tests() {...}
3.	Calling functions
5.	start_server
6.	run_tests

**Task 7**

Implement colored output for CI tests
In this task, you will create two brand new functions to add colors to the CI test results (PASSED and FAILED). 1) The first function will receive text and it will output it as is, but colored in green. It will be used to print out the PASSED tests. 2) The second function will also receive text, but it will output it in red for FAILED tests.
Once the functions are ready, run the script and ensure that the output for the PASSED tests is green and for the FAILED tests is red.

![Screenshot (402)](https://github.com/DevOpsAWSMaestro/1-Bash-Functions-/assets/134851032/5bb93bff-227c-4f28-92a2-bbe7362fb2be)

