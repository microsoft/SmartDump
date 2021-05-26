# Usage

SmartDump v0.95 x64 alpha - memory dump capture utility
Copyright (C) 2021-2031 WenJun Zhang
Microsoft Azure Integration

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
