# minishell

<h1 align="center">
	<img src="https://github.com/lkilpela/42-project-badges/blob/main/badges/minishellm.png" />
</h1>

<p align="center">
	<b><i>As beautiful as a shell</i></b><br>
</p>

<p align="center">
    <img alt="score" src="https://img.shields.io/badge/score-100%2F100-brightgreen" />
<p align="center">
    <img alt="team" src="https://img.shields.io/badge/team-2%20members-yellow" />
    <img alt="estimated time" src="https://img.shields.io/badge/time%20spent-300%20hours-blue" />
    <img alt="XP earned" src="https://img.shields.io/badge/XP%20earned-2016-orange" />
<p align="center">
	<img alt="GitHub code size in bytes" src="https://img.shields.io/github/languages/code-size/your-username/minishell?color=lightblue" />
	<img alt="Code language count" src="https://img.shields.io/github/languages/count/your-username/minishell?color=yellow" />
	<img alt="GitHub top language" src="https://img.shields.io/github/languages/top/your-username/minishell?color=blue" />
	<img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/your-username/minishell?color=green" />
</p>

## 📚 About The Project

Minishell is a 42 School project that implements a simplified Unix shell with Bash-like functionality. This project dives deep into **process control**, **file descriptor management**, and **system programming**, providing hands-on experience with core operating system concepts.

Key features:
- Interactive command line interface with prompt
- Command execution with PATH resolution
- Advanced parsing with quote and variable expansion
- Redirections and pipes
- Signal handling (Ctrl-C, Ctrl-D, Ctrl-\)
- Built-in commands (echo, cd, pwd, etc.)
- Environment variable management

## 🏁 Getting Started

1. Compile using the Makefile:
```bash
make

2. Run the shell:
```bash
./minishell

3. Exit the shell:
```bash
exit

``bas

## 🧠 Technical Implementation
### Core Architecture
Lexer: Tokenizes input into commands, arguments, and operators

Parser: Builds abstract syntax tree (AST) from tokens

Executor: Handles command execution, redirections, and pipes

Built-ins: Native shell commands implemented directly

##Key Components
Component	Description
Prompt	- Customizable prompt displaying current directory
History	- Command history accessible with arrow keys (using readline)
Expansion	- Handles VARand? environment variable expansion
Redirections	- Supports <, >, <<, >> with proper file descriptor management
Pipes	- Implements	with proper process forking and IPC
Signals	- Ctrl-C (SIGINT), Ctrl-D (EOF), Ctrl-\ (SIGQUIT) handling

###Built-in Commands
Command	Options Supported	Description
echo -	-n	Print arguments with optional newline
cd - [dir]	Change directory
pwd	-	Print working directory
export - [name[=value] ...]	Set environment variables
unset - [name ...]	Unset environment variables
env	-	Print environment
exit- [n]	Exit shell with status n

🚀 Bonus Features
Logical operators: && and || with command grouping

Wildcards: * expansion for current directory

Parentheses: Priority grouping for command execution

🧪 Testing
Recommended test cases:

```bash
# Test basic commands
echo "Hello $USER" | ./minishell

# Test pipes
cat /etc/passwd | grep $USER | wc -l

# Test redirections
echo "test" > file.txt && cat < file.txt

# Test environment variables
export TEST=value && echo $TEST

# Test signals
# Press Ctrl-C during sleep command
sleep 10

📝 Evaluation Criteria
Correctness: Matches bash behavior for specified features

Memory Management: No leaks (except readline's known leaks)

Error Handling: Graceful handling of invalid commands

Signal Handling: Proper response to Ctrl-C/D/\

Bonus: Logical operators and wildcard implementation

### 🛠️ Installation & Usage

1. Clone the repository:
```bash
git clone https://github.com/your-username/minishell.git
