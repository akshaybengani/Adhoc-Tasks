# Tasks and Solutions
This file contains all the tasks and thier solutions given in the period of Adhoc Networks Summer Training Program 2019. Tasks are given on daily basis and they are related to Linux, AWS, Redhat, etc.

# Day 1 (03/06/2019)
Notes for Day 1 are mentioned [here](https://github.com/akshaybengani/Adhoc-Notes/blob/master/Day1.md) in detail.

## Task 1 Change the Monitor view from desktop to downloads for a particular user

*   There is a file called ```user-dirs.dirs``` in ```~/.config```
*   Edit the Desktop entry with Downloads 

## Task 2 First Command Should Always give error
*   Pending 
## Task 3 Concept of Recycle Bin why it is too fast to delete a file
*   When we delete a file it basically clears the entry of the file in inode table. Which means that the data of the file exist but it is not accessible without the inode table entry.
## Task 4 Create a 5GB file and copy it 3 Times, but take size only 1 time
*   Pending
## Task 5 What happened on Spetember 1752
*   The julian calender is 365.25 days long while the perfect Gregorian calender is precisely 365.24219 days long, which means that when the britishers adopted the gee.. calender they are 13 days ahead of the gee.. calender as such on September 03 1752 the britishers ommit 13 days from thier calender and since now we have these empty 13 days not showing in our system calender.
## Task 6 Create N number of Folders in Windows using loop 
*   We can use windows bash scripting ```for``` loop for this task
```
for /l %i in (1,1,50) do mkdir dirname%i
```
*   Here ```%i``` is the counter variable and (1,1,50) means (Starting point, Increment size, End point)
## Task 7 Check at which location of RAM a variable takes memory and how much
*   Pending
## Task 8 Create 500 variables and check its memory with comparison to null and a value
*   To do this I have used a liberary called ```memoryprofiler``` which gives a tabular output of each variable taking how much memory.
*   To run this program install a liberary from pip
```
pip install memory-profiler
```
*   Since this program contains annotations so we need to specify it while running the program
```
$ python -m memory_profiler example.py
```
*   Finally the program
```python
@profile
def my_func():
    a = [1] * (10 ** 6)
    b = [2] * (2 * 10 ** 7)
    del b
    return a

if __name__ == '__main__':
    my_func()
```
*   For more information about memory-profiler [visit](https://pypi.org/project/memory-profiler/)
# Day 2 
Notes for Day 2 are mentioned [here](https://github.com/akshaybengani/Adhoc-Notes/blob/master/Day2.md) in detail.
## Task 9 Display history with time in linux
* Run the below command in your terminal or paste this in ```.bashrc```
```
export HISTTIMEFORMAT='%F %T %t'
```
## Task 10 Update history by file in ```.bash_history``` without reboot or logout
*   Close all the terminal instances then edit the ```.bash_history``` file and then reopen it or use source.
## Task 11 Install VLC in windows without GUI interaction
```
vlc.exe /L=1033 /S  
```
*   ```/L``` parameter is for Language Selection and English Language is taken as 1033 according to bash scripting.
*   ```/S``` is for setup parameter
*   This will install your software without opening any GUI or such.
*   For more information about installing VLC [click here](https://wiki.videolan.org/Documentation:Installing_VLC/
)
## Task 12 Find use cases of tuple in real life
*   Tuples are used for grouping data
*   Tuple assignment, Act as a return value
*   Composability of Data Structures
*   For more information [Click Here](http://openbookproject.net/thinkcs/python/english3e/tuples.html
)
# Day 3 
Notes for Day 3 are mentioned [here](https://github.com/akshaybengani/Adhoc-Notes/blob/master/Day3.md) in detail.
## Task 13 Application will not start with icons but will start with terminal
*   For completing this task we need a linux operating system with GUI.
*   So In order to this we need a package called ```alacarte``` which is freely available both in ```yum``` package manager and ```debian``` package managers.
*   You can install it by
```
yum install alacarte
apt-get install alacarte
```
*   By installing this package you will get a ```Main Menu``` named application in your application drawer.
*   Open that and choose the application you want to edit.
*   Then Double click that and edit the command path to something different.
*   This will modify the icon code by changing the actual path of the execution file.
*   Since now the application will not open from icon it will be opened by the terminal only until you fix that again.
## Task 14 How to write hello World in a directory
*   Pending
## Task 15 No of lines word characters count in python
*   To do this task you should have knowledge about file handling and string functions. If you want to learn more about these I have my personal notes [here](https://github.com/akshaybengani/Python-tutorials) check them out.
```py
filename = input("Please Enter a file name ")
myfile=open(filename)

lineCount = 0
wordCount = 0
charCount = 0
for lines in myfile:
    lineCount = lineCount + 1
    wordCount = wordCount + len(lines.split())
    charCount = charCount + len(lines)

print("No of Lines      :   ",lineCount)
print("No of Words      :   ",wordCount)
print("No of Characters :   ",charCount)
```
## Task 16 Count no of lines word character without saving data in a file
*   Run this program and this will ask user to enter input and to stop the input statement I have specified to use a word ```done``` to break the loop and give results.
*   Since this program will run on RAM there is no additional file write on hard disk or any other secondary storage.
```py
wordCount = 0
lineCount = 0
charCount = 0

print("Enter input \nType 'done' to end\n")

while True:
    line = input()
    if line=='done':
        break
    else:
        lineCount = lineCount + 1
        wordCount = wordCount + len(line.split())
        charCount = charCount + len(line)    

print("Number of lines      :   ",lineCount)
print("Number of Words      :   ",wordCount)
print("Number of Chars      :   ",charCount)
```
## Task 17 Search hello and then save top 5 URL in a list and then open top 5 url or all the search terms and then again save in a list and finally print that.
*   Pending
# Day 4
Notes for Day 4 are mentioned [here](https://github.com/akshaybengani/Adhoc-Notes/blob/master/Day4.md) in detail.
## Task 18 Connect RedHat with GUI
*   Pending
## Task 19 Write code in python to connect to SSH without putty
*   Pending
## Task 20 How to remove read and write permission from a file or directory for root or admin user
*   Pending
## List how many people are in a group find that list
*   
*   For more information click [here](https://www.cyberciti.biz/faq/linux-list-all-members-of-a-group/)














