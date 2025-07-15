# Things to Know

## what is a Shell?
A shell is a command-line interface that allows users to interact with the operating system. It's a program that takes input from the user (commands), interprets it, and passes it to the system for execution.
Examples of popular shells include:

- Bash (Bourne Again Shell)

- Zsh (Z Shell)

- Sh (Bourne Shell)

- Csh (C Shell)

- Ksh (Korn Shell)

## what is a Shell script? 
A shell script is a simple text file that contains a series of commands written for the Unix/Linux shell (like bash, sh, or zsh). When you run this script, the shell executes each command in order.

it is  like a to-do list for your computer to automate tasks like:

- Running programs

- Setting up environments

- Launching tools/scripts with one command

## TCL script VS Shell script
| Feature               | **TCL Script** (`.tcl`)                                                              | **Shell Script** (`.sh`)                                                |
| --------------------- | ------------------------------------------------------------------------------------ | ----------------------------------------------------------------------- |
| 🔤 **Language**       | Written in **TCL** (Tool Command Language)                                           | Written in **Shell scripting language** (e.g., Bash)                    |
| 🔧 **Used For**       | Automating **EDA tools**, parsing files, scripting inside tools                      | Automating **OS-level tasks**, file handling, launching programs        |
| ▶️ **Run Using**      | `tclsh script.tcl`                                                                   | `bash script.sh` or `./script.sh`                                       |
| 📄 **File Extension** | `.tcl`                                                                               | `.sh` (or none, but with executable permission)                         |
| 📚 **Functionality**  | More like a **programming language** – supports variables, loops, arrays, procedures | More like **command sequences** – runs OS commands, calls other scripts |
| ⚙️ **Common Uses**    | Parsing Excel, generating reports, controlling flow in VLSI/EDA tools                | Setting paths, launching TCL scripts, automating CLI processes          |
| 🤝 **Together**       | Often **called from a shell script**                                                 | Can **call a TCL script** inside it                                     |


The shell script is the launcher.
The TCL script is the logic engine.

## what is a shebang line?
A shebang line is the very first line in a script file that tells the operating system which interpreter to use to run the script.
- #! is called a shebang

- It must be the first two characters in the file

- It’s followed by the full path to the interpreter (like Bash, tcsh, Python, etc.)

Without it, the system doesn’t know which language (bash, tcsh, python, etc.) the script is written in — so it may:

❌ Throw an error

❌ Use the wrong shell (e.g., sh instead of tcsh)

❌ Misinterpret the syntax (leading to bugs like “command not found”)

## Argument indexing in shell vs TCL
shell - $argv[1], $argv[2]
TCL - lindex $argv 0 , lindex $argv 1
