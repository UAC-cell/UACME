
# UACMe
Defeating Windows User Account Control by abusing built-in Windows AutoElevate behavior.
This project demonstrates multiple UAC bypass techniques and serves as an educational resource for understanding Windows security mechanisms.

> ⚠️ **Warning**: This tool demonstrates security vulnerabilities that could be exploited maliciously. Use responsibly and only in controlled environments.

# System Requirements
* Operating Systems: Windows 7/8/8.1/10/11 (including windows 11 25H2)
* User Account: Administrator account with UAC set on default settings
* UAC: Default (standard) configuration

# Updated Behavior

In older versions, UAC bypass required selecting specific method_number values depending on OS version.
This update removes that limitation:
✔ Cleaner Codebase: Consolidation removes duplicated logic from older methods and prepares the project for future updates.

✔ All operations are now unified under Method 43

* A single method now works consistently across supported Windows versions.

* Duplicate logic and outdated method implementations were consolidated.

* The long-standing UAC bypass failure on Windows 11 25H2 has been resolved.


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
# Protection Measures
The most effective protection against UAC bypass techniques is using an account without administrative privileges.

# Build instructions
UACMe is written in C and requires Microsoft Visual Studio 2019 or later to build from source.

### Prerequisites
IDE: Microsoft Visual Studio 2019 or 2022
SDK Requirements:
Windows 8.1 or Windows 10 SDK (tested with 19041 version)
NET Framework SDK (tested with 4.8 version)

# Legal Disclaimer
* This tool is provided for educational and research purposes only
* We do not take any responsibility for this tool being used in malicious activities
* We have no affiliation with any "security company" using this code for commercial activities
* This GitHub repository (hfiref0x/UACME) is the only genuine source for UACMe code
