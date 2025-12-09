
# UACMe
Defeating Windows User Account Control by abusing built-in Windows AutoElevate backdoor. This project demonstrates various UAC bypass techniques and serves as an educational resource for understanding Windows security mechanisms.

> ⚠️ **Warning**: This tool demonstrates security vulnerabilities that could be exploited maliciously. Use responsibly and only in controlled environments.

# System Requirements
* Operating Systems: Windows 7/8/8.1/10/11 (including windows 11 25H2)
* User Account: Administrator account with UAC set on default settings

# Usage
Run the executable from command line using the following syntax:
```
akagi32.exe 43 [Optional_Command]
```
or
```
akagi64.exe 43 [Optional_Command]
```
* **Optional_Command**: Full path to an executable file to run with elevated privileges
  * If omitted, the program will launch an elevated command prompt (%systemroot%\system32\cmd.exe)
### Examples:
```
akagi32.exe 43 c:\windows\system32\calc.exe
akagi64.exe 43 c:\windows\system32\charmap.exe
```
