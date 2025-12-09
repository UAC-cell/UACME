
# UACMe
Defeating Windows User Account Control by abusing built-in Windows AutoElevate backdoor. This project demonstrates various UAC bypass techniques and serves as an educational resource for understanding Windows security mechanisms.

> ⚠️ **Warning**: This tool demonstrates security vulnerabilities that could be exploited maliciously. Use responsibly and only in controlled environments.

# System Requirements
* Operating Systems: Windows 7/8/8.1/10/11 (including windows 11 25H2)
* User Account: Administrator account with UAC set on default settings

# Updated issues
* In previous versions, UAC was performed using a user-specified method for each system among several method_numbers,
but the updated version overcomes this problem and implements this operation on all systems using a single method.
That is, method_number was unified to 43.

* Additionally, the UAC bypass issue that was impossible to achieve in the Windows 25H2 system environment was resolved.

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
