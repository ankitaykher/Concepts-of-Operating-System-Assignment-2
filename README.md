# Concepts-of-Operating-System-Assignment-2
---------------------------------------------------------------------------------------------------- part-A -----------------------------------------------------------------------------------------------------------
What will the following commands do?
echo "Hello, World!"                               //  this command print the output

name="Productive"                              //  name is assign value 

touch file.txt                              // create file from this command

 ls -a                                    // list all folder and directory includimg hiddend one

 rm file.txt                            // remove file.txt

 cp file1.txt file2.txt              // copy file 1 from to file2

 mv file.txt /path/to/directory/    // move file path to dir

 chmod 755 script.sh              // chane mode give permission to script.sh

 grep "pattern" file.txt         //  search for specific what you want like check pattern of txt file

 kill PID                       // Send a signal for process id

 mkdir mydir && cd mydir && touch file.txt && echo "Hello, World!" > file.txt && cat file.txt  // makr directory && Logical AND operator runs the next command only if the previous command succeeds make txt file && print command to                                                                                                          file.txt  and diplay help hot cat

  ls -l | grep ".txt"                      // Lists all files and directories in the current directory (|)  this call pipe send output next command and search specific file .txt

  cat file1.txt file2.txt | sort | uniq   // display file.1 and file 2 and send output for sorting uniq line which in include in this file

  ls -l | grep "^d"            //Lists all files and directories in the current directory and send output (|) and search specific  (d) ilters lines that start with d 

  grep -r "pattern" /path/to/directory/      //Tells grep to search inside all files in the specified directory and its subdirectories (-r) stands for recursive Search recursively (-r) inside all files and subdirectories of                                                                   /path/to/directory/ for the word or pattern "pattern" and print all matching lines along with their file names.

  cat file1.txt file2.txt | sort | uniq –d        // Concatenate file1.txt and file2.txt (cat file1.txt file2.txt), sort all lines alphabetically (sort), and then print only the lines that appear more than once (uniq -d), effectively                                                          showing duplicates across the two files.

  chmod 644 file.txt                          // Change the permissions of file.txt so that the owner can read and write  644 -> 6 owner  read + write 4+2=6 ,4 group ,4 other


  cp -r source_directory destination_directory   //  copy all files inside subdirectory into destination_directory
  
  find /path/to/search -name "*.txt"            // find path and search name Search from /path/to/search for all files ending with .txt and print their paths.
  
  chmod u+x file.txt                          // change mode add execution permission for owner 
  
  echo $PATH                                //  Show directories where commands are searched.


              ------------------------------------------------------------------------------- Part -B ---------------------------------------------------------------------------------------------

  Identify True or False:

  Identify True or False:
1. ls is used to list files and directories in a directory.
->   true
3. mv is used to move files and directories.
-> true
   
5. cd is used to copy files and directories.
->false

7. pwd stands for "print working directory" and displays the current directory
->true

9. grep is used to search for patterns in files.
->true

6. chmod 755 file.txt gives read, write, and execute permissions to the owner, and read and execute permissions to group and others.
   true
   
8. mkdir -p directory1/directory2 creates nested directories, creating directory2 inside directory1 if directory1 does not exist.
-> true
   
10. rm -rf file.txt deletes a file forcefully without confirmation
->  true


Identify the Incorrect Commands:

1. chmodx is used to change file permissions.
->
3. cpy is used to copy files and directories.
->
5. mkfile is used to create a new file.
  
7. catx is used to concatenate files.
   
9. rn is used to rename files.

-> All the command Incorrect


                                                                                                                part - c



Question 1: Write a shell script that prints "Hello, World!" to the terminal.

->echo "Hello world!"

Question 2: Declare a variable named "name" and assign the value "CDAC Mumbai" to it. Print the
value of the variable.

-> #!/bin/bash
   name="CDAC Mumbai"
   echo "The value of name is: $name"

Question 3: Write a shell script that takes a number as input from the user and prints it.
-> 
read -p "Enter a number: " number
echo "You entered: $number"


Question 4: Write a shell script that performs addition of two numbers (e.g., 5 and 3) and prints the
result.

-> num1 = 5

   num2 = 3
   
   sum=$((num1 + num2))

   echo " sum the number  $num1 and $num2 is : $sum
  
Question 5: Write a shell script that takes a number as input and prints "Even" if it is even, otherwise
prints "Odd".
-> #!/bin/bash
read -p "Enter a number: " number
if [ $((number % 2)) -eq 0 ]; then
    echo "Even"
else
    echo "Odd"
fi


Question 6: Write a shell script that uses a for loop to print numbers from 1 to 5.
for i (1..5)

do 

echo $i

done

Question 7: Write a shell script that uses a while loop to print numbers from 1 to 5.

#!/bin/bash

i=1
while [ $i -le 5 ]
do
    echo $i
    ((i++))
    
done




Question 8: Write a shell script that checks if a file named "file.txt" exists in the current directory. If it does, print "File exists", otherwise, print "File does not exist".
->

#!/bin/bash

if [ -e file.txt ];       then

    echo "File is exists"
    
else

    echo "File does not exist"
    
fi


Question 9: Write a shell script that uses the if statement to check if a number is greater than 10 and prints a message accordingly.

#!/bin/bash

read -p "Enter a number: " number

if [ $number -gt 10 ]; then

    echo "$number is greater than 10"
    
else


    echo "$number is not greater than 10"
    
    
fi


Question 10: Write a shell script that uses nested for loops to print a multiplication table for numbers from 1 to 5. The output should be formatted nicely, with each row representing a number and each column representing the multiplication result for that number.


#!/bin/bash

for i in {1..5}

do

    for j in {1..5}
    
    do
    
        printf "%d\t" $((i * j))
        
    done
    
    echo 
    
done



Question 11: Write a shell script that uses a while loop to read numbers from the user until the user enters a negative number. For each positive number entered, print its square. Use the break statement to exit the loop when a negative number is entered.

#!/bin/bash

while true

do
    read -p "Enter a number (negative number to exit): " number
    
        if [ $num -lt 0 ]; then
        
                echo "Negative number entered. Exiting..."
                
                        break
                        
                            fi
                            
                                sq=$((number * number))
                                
                                    echo "The square of $number is: $sq"
                                    
done



part-e

1. Consider the following processes with arrival times and burst times:
| Process | Arrival Time | Burst Time |
|---------|--------------|------------|
| P1 | 0 | 5 |
| P2 | 1 | 3 |
| P3 | 2 | 6 |
Calculate the average waiting time using First-Come, First-Served (FCFS) scheduling.
2. Consider the following processes with arrival times and burst times:
| Process | Arrival Time | Burst Time |
|---------|--------------|------------|
| P1 | 0 | 3 |
| P2 | 1 | 5 |
| P3 | 2 | 1 |
| P4 | 3 | 4 |
Calculate the average turnaround time using Shortest Job First (SJF) scheduling.

3. Consider the following processes with arrival times, burst times, and priorities (lower number
indicates higher priority):
| Process | Arrival Time | Burst Time | Priority |
|---------|--------------|------------|----------|
| P1 | 0 | 6 | 3 |
| P2 | 1 | 4 | 1 |
| P3 | 2 | 7 | 4 |
| P4 | 3 | 2 | 2 |
Calculate the average waiting time using Priority Scheduling.
4. Consider the following processes with arrival times and burst times, and the time quantum for
Round Robin scheduling is 2 units:
| Process | Arrival Time | Burst Time |
|---------|--------------|------------|
| P1 | 0 | 4 |
| P2 | 1 | 5 |
| P3 | 2 | 2 |
| P4 | 3 | 3 |
Calculate the average turnaround time using Round Robin scheduling.
5. Consider a program that uses the fork() system call to create a child process. Initially, the parent
process has a variable x with a value of 5. After forking, both the parent and child processes
increment the value of x by 1.
What will be the final values of x in the parent and child processes after the fork() call?

  



  



  







 




