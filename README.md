# Miscellaneous TestStand Solutions
In this repository, I collect TestStand-based solutions to various problems. The current collection contains:
- **XML to HTML Report Converter** - A sequence to convert TestStand reports in ATML (XML) format to HTML. The solution uses the *msxml6.dll* library preinstalled with Windows. The *msxml* is called as ActiveX Action step.
- **Output to Stream** - A sequence demonstrating the use of streams for create output logs. The solution uses *Statements* instead of *Stream* steps.

<p align = "center">
<img src = "https://github.com/425J/TestStandMiscellaneous/blob/main/Output%20to%20Stream/img/Output%20to%20Stream%20Demo.png?raw=true"></br>
<i>Output to Stream</i>
</p>

- **LabVIEW Compiled Object Cache Preparation** - A sequence demonstrating how to programmatically open a LabVIEW project in the IDE and gracefully close it to generate LabVIEW compiled object cache. If in TestStand the LabVIEW adapter is configured to use the LabVIEW Runtime Engine, and the sequence refers to LabVIEW sources (`*.vi` files) that have the *separate compiled code from source file* option selected, then the LabVIEW IDE must first generate a compiled object cache (`[LabVIEW Data]\VIObjCache`) in order not to receive an error. This example can be useful when creating test sequences for automatic LabVIEW project analysis. However, for such a configuration to make sense, the IDE would have to be made available on the remote computer, and to call this sequence, it would have to use the *Use Remote Computer* option. In this scenario, there would be one remote computer with a LabVIEW development license (and probably basic TestStand) as a compiler and tester with TestStand (and without LabVIEW license) to execute sequences using LabVIEW Runtime Engine only.
