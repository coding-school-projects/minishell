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
	<img alt="GitHub code size in bytes" src="https://img.shields.io/github/languages/code-size/senthilpoo10/minishell?color=lightblue" />
	<img alt="Code language count" src="https://img.shields.io/github/languages/count/senthilpoo10/minishell?color=yellow" />
	<img alt="GitHub top language" src="https://img.shields.io/github/languages/top/senthilpoo10/minishell?color=blue" />
	<img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/senthilpoo10/minishell?color=green" />
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

## 🧠 Technical Implementation
### Core Architecture
Lexer: Tokenizes input into commands, arguments, and operators

Parser: Builds abstract syntax tree (AST) from tokens

Executor: Handles command execution, redirections, and pipes

Built-ins: Native shell commands implemented directly


### Key Components
| Component        | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| **Prompt**       | Customizable prompt showing current directory with ANSI colors              |
| **History**      | Persistent command history with up/down arrow navigation (using readline)   |
| **Lexer**        | Tokenizes input into commands, arguments, operators, and redirections       |
| **Parser**       | Validates syntax and builds execution tree with proper operator precedence  |
| **Expansion**    | Handles `$VAR` environment variables and `$?` exit status expansion        |
| **Redirections** | Manages `<` (input), `>` (output), `<<` (heredoc), `>>` (append)           |
| **Pipes**        | Implements `|` with proper process forking and inter-process communication |
| **Signals**      | Handles Ctrl-C (SIGINT), Ctrl-D (EOF), Ctrl-\ (SIGQUIT) like bash          |

### Built-in Commands
| Command   | Options Supported          | Description                                                                 |
|-----------|----------------------------|-----------------------------------------------------------------------------|
| `echo`    | `-n`                       | Prints arguments without trailing newline when `-n` specified               |
| `cd`      | `[dir]` or `~`             | Changes directory with path resolution (`~` for home, `-` for previous)     |
| `pwd`     | None                       | Prints absolute path of current working directory                          |
| `export`  | `[name[=value]]`           | Sets environment variables (no args prints all exported vars)               |
| `unset`   | `[name]`                   | Removes environment variables                                               |
| `env`     | None                       | Prints all environment variables                                            |
| `exit`    | `[n]`                      | Exits shell with status `n` (default 0)                                    |


## 🚀 Bonus Features
Logical operators: && and || with command grouping

Wildcards: * expansion for current directory

Parentheses: Priority grouping for command execution

 ## 📝 Evaluation Criteria
Correctness: Matches bash behavior for specified features

Memory Management: No leaks (except readline's known leaks)

Error Handling: Graceful handling of invalid commands

Signal Handling: Proper response to Ctrl-C/D/\

Bonus: Logical operators and wildcard implementation

### 🛠️ Installation & Usage

1. Clone the repository:
```bash
git clone https://github.com/your-username/minishell.git
