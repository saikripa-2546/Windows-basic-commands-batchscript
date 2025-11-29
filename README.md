# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"
<img width="681" height="86" alt="img1" src="https://github.com/user-attachments/assets/ef12ed65-dedc-4255-af8a-ca8b83f40fab" />



## COMMAND AND OUTPUT

Remove the directory "my-folder"
<img width="726" height="73" alt="img2" src="https://github.com/user-attachments/assets/38a94f0c-1426-491d-b2af-9400cada8e77" />


## COMMAND AND OUTPUT


Create the file Rose.txt
<img width="721" height="77" alt="img3" src="https://github.com/user-attachments/assets/ecba0162-7b70-48b5-8951-d84e4a58b3e3" />


## COMMAND AND OUTPUT

Create the file hello.txt using echo and redirection
<img width="798" height="58" alt="img4" src="https://github.com/user-attachments/assets/0377fad6-0b40-4f1f-ac5f-5fc8f25c250a" />

## COMMAND AND OUTPUT

Copy the file hello.txt into the file hello1.txt
<img width="825" height="88" alt="img5" src="https://github.com/user-attachments/assets/75abb075-b946-4229-954c-ed0ef55e5825" />

## COMMAND AND OUTPUT

Remove the file hello1.txt
<img width="677" height="57" alt="img6" src="https://github.com/user-attachments/assets/a7658557-b097-4148-b4fa-25f7d2ec19bc" />


## COMMAND AND OUTPUT

List out all the associated file extensions 
<img width="677" height="548" alt="img8" src="https://github.com/user-attachments/assets/18a3f0f5-30a3-4e78-883f-5d5aa373d083" />


## COMMAND AND OUTPUT


Compare the file hello.txt and rose.txt
<img width="746" height="127" alt="img9" src="https://github.com/user-attachments/assets/fa73ca8b-e45f-454a-94ce-81ba6b85feb9" />

## COMMAND AND OUTPUT

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
---

## BATCH PROGRAM:
```
@echo off
set name=John
echo Hello, %name%
pause
```
---

## OUTPUT
<img width="625" height="70" alt="img10" src="https://github.com/user-attachments/assets/68129a18-561a-4e8d-9147-6699741adba7" />


2.Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
---

## BATCH PROGRAM
```
 batch
@echo off
:loop
set /p num=Enter a number: 
set /a rem=%num% %% 2

if %rem%==0 (
    echo %num% is Even
) else (
    echo %num% is Odd
)

:ask
set /p ans=Do you want to check another number? (Y/N): 
if /I "%ans%"=="Y" goto loop
if /I "%ans%"=="N" goto end
echo Invalid input. Please enter Y or N.
goto ask

:end
echo Thank you!
pause
```
---
## OUTPUT

<img width="661" height="198" alt="img11" src="https://github.com/user-attachments/assets/8e3b3b37-7f39-40e6-b1f9-0fac5b4f054b" />


3.Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

## BATCH PROGRAM:
```
@echo off
for /L %%i in (1,1,5) do (
    echo Number: %%i
)
pause
```
## OUTPUT
<img width="626" height="151" alt="img12" src="https://github.com/user-attachments/assets/326d6da5-fdd5-433e-bcdd-bd6d9ef34e53" />


4.Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
---
## BATCH PROGRAM:
```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```
## OUTPUT

<img width="666" height="67" alt="img13" src="https://github.com/user-attachments/assets/838f232f-4644-4ce6-8b8e-7ca69542ea5b" />

5.Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
## BATCH PROGRAM
```
@echo off
:menu
cls
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option (1-3): 

if "%choice%"=="1" goto hello
if "%choice%"=="2" goto create
if "%choice%"=="3" goto exit
echo Invalid choice.
pause
goto menu

:hello
echo Hello, World!
pause
goto menu

:create
echo This is a new file > newfile.txt
echo File newfile.txt created.
pause
goto menu

:exit
echo Goodbye!
pause
exit

```
## OUTPUT

<img width="292" height="132" alt="img16" src="https://github.com/user-attachments/assets/523c15df-fd42-4bea-b785-1a9a1220a7ca" />
<img width="307" height="135" alt="img15" src="https://github.com/user-attachments/assets/b601ce6f-5f72-4fe6-9b77-5d6a48b8a1a5" />
<img width="297" height="128" alt="img14" src="https://github.com/user-attachments/assets/a7ffa852-c056-4f5e-bf09-647f5459bc38" />

# RESULT:
The commands/batch files are executed successfully.
