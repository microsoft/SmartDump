# Usage:

SmartDump v0.99 x86/x64 alpha - memory dump capture utility

**Options:**

    -p      PID of target process.
 
    -ma     Manual full memory dump.
 
    -d      Collect number of dumps.
 
    -n      Number of exceptions to be captured. Default is 5. Set to 0 means unlimited.
 
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

        - Capture a dump based on specified address of breakpoint:
                SmartDump.exe -d 1 -p 4567 -a 7a64e9d0 -n 1

The following are several sample commands that uses the tool with Kudu debug console. 

1) Show options and examples

![image](https://user-images.githubusercontent.com/32285008/121564667-4b07e300-ca4e-11eb-9b7a-ed1ec223ebb5.png)

2) Monitor and display exceptions

![image](https://user-images.githubusercontent.com/32285008/121565037-a934c600-ca4e-11eb-9f3d-f287933ed944.png)

3) Capture a manual dump

![image](https://user-images.githubusercontent.com/32285008/121565536-19434c00-ca4f-11eb-9312-e4e8f6086c4b.png)

4) Capture two exception dumps based on filter string

![image](https://user-images.githubusercontent.com/32285008/121566060-b56d5300-ca4f-11eb-8ff3-5caca299f0b8.png)

5) Exclude/filter uninterested exceptions based on specified strings delimited with '|'

![image](https://user-images.githubusercontent.com/32285008/121568609-7391dc00-ca52-11eb-83d6-696c973e4a06.png)

6) Collect dump based on specified address of breakpoint

![image](https://user-images.githubusercontent.com/32285008/121567772-8bb52b80-ca51-11eb-8287-916f24678d40.png)
![image](https://user-images.githubusercontent.com/32285008/121567944-b7d0ac80-ca51-11eb-9540-cad30f0fa081.png)

7) Capture against process of onpromise environment

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
