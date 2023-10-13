### Installation
VS Code was already installed back in year 1. Installing the rest on the list (Verilator, riscv-gnu-toolchain, gtkwave) went smoothly, just followed the instructions under Installation for Windows 10 and 11. 
Note: skipped step 4 because this year we need WSL2 not WSL1. 
Note: for step 5 don't run wsl --set-version Ubuntu-22.04 1 (which just sets the WSL version to 1) because we need WSL2 not 1. 
Note: can check the version of WSL by running the command **wsl -l -v** in PowerShell or Windows Command Prompt.
Note: the workspace can be found in file explorer under Linux -> Ubuntu-22.04 -> home -> adrian -> Documents -> iac -> lab0-devtools.
### Toolchain Test (Makefile Test)
The file named Makefile under the IAC-autumn workspace you can think of it as something that contains a bunch of "functions" which are called scripts (default, clean, build, tb_toolchain, tb_verilator) which you can call in the terminal and it'll run the commands under that script (the lines beginning with @). The purpose of this is say you have 5 commands you wanna run but you dun wanna manually type all five commands in the terminal. So you just make a script in the Makefile that runs all 5 commands when you call the script in the terminal.
Note: @echo prints stuff

Running the commands make tb_verilator and make tb_toolchain in the terminal just runs the scripts tb_verilator and tb_toolchain which are defined in the Makefile file.

The command make tb_verilator just converts the test file mod_test.sv under the rtl folder in the workspace from a system verilog file into a c++ file so that we can run it.
