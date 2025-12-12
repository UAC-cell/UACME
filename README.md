
# UACME(version 3.7.2)
Defeating Windows User Account Control by abusing built-in Windows AutoElevate behavior(UAC-Bypass).
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

# References
Windows 7 UAC whitelist, http://www.pretentiousname.com/misc/win7_uac_whitelist2.html
Malicious Application Compatibility Shims, https://www.blackhat.com/docs/eu-15/materials/eu-15-Pierce-Defending-Against-Malicious-Application-Compatibility-Shims-wp.pdf
Junfeng Zhang from WinSxS dev team blog, https://blogs.msdn.microsoft.com/junfeng/
Beyond good ol' Run key, series of articles, http://www.hexacorn.com/blog
KernelMode.Info UACMe thread, https://www.kernelmode.info/forum/viewtopicf985.html?f=11&t=3643
Command Injection/Elevation - Environment Variables Revisited, https://breakingmalware.com/vulnerabilities/command-injection-and-elevation-environment-variables-revisited
"Fileless" UAC Bypass Using eventvwr.exe and Registry Hijacking, https://enigma0x3.net/2016/08/15/fileless-uac-bypass-using-eventvwr-exe-and-registry-hijacking/
Bypassing UAC on Windows 10 using Disk Cleanup, https://enigma0x3.net/2016/07/22/bypassing-uac-on-windows-10-using-disk-cleanup/
Using IARPUninstallStringLauncher COM interface to bypass UAC, http://www.freebuf.com/articles/system/116611.html
Bypassing UAC using App Paths, https://enigma0x3.net/2017/03/14/bypassing-uac-using-app-paths/
"Fileless" UAC Bypass using sdclt.exe, https://enigma0x3.net/2017/03/17/fileless-uac-bypass-using-sdclt-exe/
UAC Bypass or story about three escalations, https://habrahabr.ru/company/pm/blog/328008/
Exploiting Environment Variables in Scheduled Tasks for UAC Bypass, https://tyranidslair.blogspot.ru/2017/05/exploiting-environment-variables-in.html
First entry: Welcome and fileless UAC bypass, https://winscripting.blog/2017/05/12/first-entry-welcome-and-uac-bypass/
Reading Your Way Around UAC in 3 parts:
https://tyranidslair.blogspot.ru/2017/05/reading-your-way-around-uac-part-1.html
https://tyranidslair.blogspot.ru/2017/05/reading-your-way-around-uac-part-2.html
https://tyranidslair.blogspot.ru/2017/05/reading-your-way-around-uac-part-3.html
Research on CMSTP.exe, https://msitpros.com/?p=3960
UAC bypass via elevated .NET applications, https://offsec.provadys.com/UAC-bypass-dotnet.html
UAC Bypass by Mocking Trusted Directories, https://medium.com/tenable-techblog/uac-bypass-by-mocking-trusted-directories-24a96675f6e
Yet another sdclt UAC bypass, http://blog.sevagas.com/?Yet-another-sdclt-UAC-bypass
UAC Bypass via SystemPropertiesAdvanced.exe and DLL Hijacking, https://egre55.github.io/system-properties-uac-bypass/
Accessing Access Tokens for UIAccess, https://tyranidslair.blogspot.com/2019/02/accessing-access-tokens-for-uiaccess.html
Fileless UAC Bypass in Windows Store Binary, https://www.activecyber.us/1/post/2019/03/windows-uac-bypass.html
Calling Local Windows RPC Servers from .NET, https://googleprojectzero.blogspot.com/2019/12/calling-local-windows-rpc-servers-from.html
Microsoft Windows 10 UAC bypass local privilege escalation exploit, https://packetstormsecurity.com/files/155927/Microsoft-Windows-10-Local-Privilege-Escalation.html
UACMe 3.5, WD and the ways of mitigation, https://swapcontext.blogspot.com/2020/10/uacme-35-wd-and-ways-of-mitigation.html
UAC bypasses from COMAutoApprovalList, https://swapcontext.blogspot.com/2020/11/uac-bypasses-from-comautoapprovallist.html
Utilizing Programmatic Identifiers (ProgIDs) for UAC Bypasses, https://v3ded.github.io/redteam/utilizing-programmatic-identifiers-progids-for-uac-bypasses
MSDT DLL Hijack UAC bypass, https://blog.sevagas.com/?MSDT-DLL-Hijack-UAC-bypass
UAC bypass through .Net Deserialization vulnerability in eventvwr.exe, https://twitter.com/orange_8361/status/1518970259868626944
Advanced Windows Task Scheduler Playbook - Part.2 from COM to UAC bypass and get SYSTEM directly, http://www.zcgonvh.com/post/Advanced_Windows_Task_Scheduler_Playbook-Part.2_from_COM_to_UAC_bypass_and_get_SYSTEM_dirtectly.html
Bypassing UAC with SSPI Datagram Contexts, https://splintercod3.blogspot.com/p/bypassing-uac-with-sspi-datagram.html
Mitigate some Exploits for Windows’® UAC, https://skanthak.hier-im-netz.de/uacamole.html
