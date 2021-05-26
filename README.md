# Usage:

SmartDump v0.95 x64 alpha - memory dump capture utility

Options:

        -p     PID of target process.

        -ma    Manual full memory dump.

        -d     Collect number of dumps.

        -n     Number of exceptions to be captured.

        -f     Filter exception based on specified string.

        -a     Address of breakpoint.

        -o     Output path of dump(s).

        -h     Or -?/-help. Display usage and examples.

Examples:
------------------------------------------

        - Write a manual dump against process with id 4567:
                SmartDump.exe -ma -p 4567

        - Monitor and print 10 managed exceptions against process with id 4567:
                SmartDump.exe -p 4567 -n 10

        - Capture two dumps based on filtered managed exception:
                SmartDump.exe -p 4567 -f "Object reference not set" -n 10 -d 2

        - Capture a dump based on specified address of breakpoint:
                SmartDump.exe -d 1 -p 4567 -a 7a64e9d0 -n 1

The following are several sample commands that uses the tool with Kudu debug console. 

1) Show options and examples

![image](https://user-images.githubusercontent.com/32285008/119694737-16a5fb80-be80-11eb-883b-ea2b48b2221f.png)

2) Monitor and display exceptions

![image](https://user-images.githubusercontent.com/32285008/119694993-566ce300-be80-11eb-8e5e-6b787d160d0f.png)

3) Capture a manual dump

![image](https://user-images.githubusercontent.com/32285008/119695109-72708480-be80-11eb-9adb-184e47cdc453.png)

4) Capture two exception dumps based on filter string

![image](https://user-images.githubusercontent.com/32285008/119695216-8c11cc00-be80-11eb-89a0-ab47c97499ac.png)

5) Capture dump based on specified address of breakpoint

![image](https://user-images.githubusercontent.com/32285008/119695379-aea3e500-be80-11eb-94f8-696b034b544e.png)
![image](https://user-images.githubusercontent.com/32285008/119695397-b2376c00-be80-11eb-88d0-bbc0ca2d9252.png)


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
