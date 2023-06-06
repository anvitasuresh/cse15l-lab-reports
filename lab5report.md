# Debugging
Today, we will be designing a debugging scenario by simulating a conversation that a student has with their TA regarding a problem with their code. 

## Part 1 – Debugging Scenario

### The Student's Question
Below is the conversation between the student and TA via edstem, where the student highlights the issue they had when running their bash script from lab6. 

![Image](lab5-ss6.png)
![Image](lab5-ss7.png)
![Image](lab5-ss8.png)

Here are closer images of the bash script and output for better viewing :)

![Image](lab5-ss1.png)
![Image](lab5-ss2.png)

### The TA's Response

![Image](lab5-ss9.png)

### Student's Fix
The student used the response from the TA and realized where their error occurs. After checking their current directory and seeing that it was actually grading-area, they saw that lib was not inside of this directory. Since lib stores the JUnit and hamcrest files, there will be an error in the terminal when running the bash script that the package does not exist. To fix this error, the student added `cp -r ../lib .` to line 21 in grade.sh which moves lib into grading-area and allows for the bash script to run and compile without error. 

