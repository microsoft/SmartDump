# Introduction:

SmartDump is a flexible command line utility to capture exception logs and memory dump files against a target process based on user specified settings like filter strings or memory addresses of breakpoints. This tool also focuses on addressing several scenarios that we cannot utilize some well-known and most widely used debugging tools, for example:

    1. iDNA Trace(TTT/TTD) cannot be used with Kudu console or RDP for Azure AppService related debugging.
    2. Debug Diagnostic Tool(DebugDiag) cannot be installed and used for Kudu console or RDP as well.
    3. Procdump works with Kudu and RDP but isn't able to capture managed exceptions against web hosts with .Net Core runtime.
    4. For intermittent issues, capturing iDNA Trace(TTT/TTD) may not be a suitable approach even with selective recording. 

Currently SmartDump is still under a pre-release build. New features are continuously being added. 
Bug reports, suggestions and feedback from you will be very much appreciated.

# Usage:

SmartDump v1.00 x86/x64 beta - exception and memory dump capture utility

**Options:**

    -p      PID of target process.
 
    -ma     Manual full memory dump.
 
    -d      Collect number of dumps.
 
    -n      Number of exceptions to be captured. Default is 5. Set to 0 means unlimited.
    
    -s      Skip the first number of exceptions for dump capture. This option is useful when initial exceptions cannot reflect an actual issue.
 
    -f      Filter exception based on specified string(s). Use '|' as delimiter for multiple strings.
 
    -fv     Exclude exceptions contain specified filter. Use '|' as delimiter for multiple strings.
 
    -a      Address of breakpoint.
 
    -o      Output path of dump(s).
 
    -h      Or -?/-help. Display usage and examples.

Examples:
------------------------------------------

        - Write a manual dump against process with id 4567:
                SmartDump.exe -ma -p 4567

        - Monitor and print 10 managed exceptions against process with id 4567:
                SmartDump.exe -p 4567 -n 10

        - Capture two dumps based on filtered strings of managed exceptions:
                SmartDump.exe -p 4567 -f "Object reference not set|ArgumentException" -n 10 -d 2

        - Exclude exceptions contain specified filter string from output:
                SmartDump.exe -p 4567 -n 10 -fv "InvalidOperationException|FileNotFoundException"
                
        - Skip the first 3 NullReferenceException. Capture a memory dump for the 4th one and specify output path to: c:\home\dump.
                SmartDump.exe -p 4567 -n 10 -f "NullReferenceException" -s 3 -d 1 -o c:\home\dump

        - Capture a dump based on specified address of breakpoint:
                SmartDump.exe -d 1 -p 4567 -a 7a64e9d0 -n 1

The following are several sample commands that uses the tool with Kudu debug console. 

1) Show options and examples

![image](https://user-images.githubusercontent.com/32285008/122183087-79a61380-cebd-11eb-9276-a34d6ccf1e05.png)

2) Monitor and display exceptions

![image](https://user-images.githubusercontent.com/32285008/121565037-a934c600-ca4e-11eb-9f3d-f287933ed944.png)

3) Capture a manual dump

![image](https://user-images.githubusercontent.com/32285008/121565536-19434c00-ca4f-11eb-9312-e4e8f6086c4b.png)

4) Capture two exception dumps based on filter string.

![image](https://user-images.githubusercontent.com/32285008/121566060-b56d5300-ca4f-11eb-8ff3-5caca299f0b8.png)

5) Exclude/filter uninterested exceptions based on specified strings delimited with '|'

![image](https://user-images.githubusercontent.com/32285008/121568609-7391dc00-ca52-11eb-83d6-696c973e4a06.png)

6) Collect dump based on specified address of breakpoint.

![image](https://user-images.githubusercontent.com/32285008/122042223-769f1a80-ce0c-11eb-9529-8c5ca17c6b02.png)

7) Skip the first 3 SqlException. Capture two memory dumps for the 4th and 5th ones and specify output path to: c:\home\dump.

![image](https://user-images.githubusercontent.com/32285008/122184337-b32b4e80-cebe-11eb-88f5-cf91a546e8c5.png)

8) Use SmartDump to write a log of exceptions for your site.

![image](https://user-images.githubusercontent.com/32285008/122149025-fd480c00-ce8d-11eb-8ae9-650f4367ecf3.png)
![image](https://user-images.githubusercontent.com/32285008/122149126-28326000-ce8e-11eb-9b6a-cee89a2d77bd.png)

9) Capture against process of onpromise environment

![image](https://user-images.githubusercontent.com/32285008/121570281-4f36ff00-ca54-11eb-8089-df7fb2e14924.png)


# Project

> This repo has been populated by an initial template to help get you started. Please
> make sure to update the content to build a great experience for community-building.

As the maintainer of this project, please make a few updates:

- Improving this README.MD file to provide a great experience
- Updating SUPPORT.MD with content about this project's support experience
- Understanding the security reporting process in SECURITY.MD
- Remove this section from the README

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft 
trademarks or logos is subject to and must follow 
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.
