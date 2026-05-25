# 🖥️ File Management System (Custom Shell)

A low-level file management system developed in C for Linux, featuring a custom command-line interpreter (shell), file manipulation tools, and support for pipes and redirection.

This project was developed as part of an Operating Systems course, focusing on system calls, process management, and containerization.

---

## 📦 Features

### File Management Commands

- `mostra` — Display file contents  
- `copia` — Copy files  
- `acrescenta` — Append file contents  
- `conta` — Count lines, words, and characters  
- `apaga` — Delete files  
- `informa` — Display file metadata  
- `lista` — List directory contents  
- `procura` — Search for patterns in files or stdin  

### Custom Shell

- Custom prompt (`%`)
- Command execution via `fork()` and `execvp()`
- Process synchronization with `waitpid()`
- Sequential command execution
- Built-in command: `termina` (exit)

### Advanced Features

- Output redirection (`>`)
- Input redirection (`<`)
- Pipes between commands (`|`)

### Containerization

- Fully Dockerized environment
- Automatic compilation during image build
- Ready-to-run interpreter inside container

---

## 🛠️ Technologies

- **C (Linux Programming)**
- **POSIX System Calls**
  - File management: `open`, `read`, `write`, `close`, `unlink`
  - Process management: `fork`, `execvp`, `waitpid`
  - IPC: `pipe`, `dup2`
  - File system: `stat`, `opendir`, `readdir`
- **Docker**
- **Linux / WSL**

---

## ▶️ Usage

### Run with Docker

Build the image:

```bash
docker build -t interpretador-img .
docker run -it interpretador-img
```
## 💻 Example Commands

```bash
# List directory contents
% lista

# Display file contents
% mostra ficheiro.txt

# Count lines, words and characters
% conta ficheiro.txt

# Output redirection
% lista > output.txt
% mostra output.txt

# Input redirection
% conta < ficheiro.txt

# Pipe between commands
% lista | conta

# Search using pipe
% mostra ficheiro.txt | procura palavra
```

---

## 🎓 Academic Context

This project was developed as part of the **Operating Systems** course in the **Computer Systems Engineering degree**.

It demonstrates:

- System calls for low-level file manipulation  
- Process creation and control (`fork`, `exec`, `wait`)  
- Inter-process communication using pipes  
- File descriptor redirection with `dup2`  
- Implementation of a simplified Unix-like shell  
- Containerized execution using Docker

---

## 📜 License

This project is provided for **educational purposes only**.

You are free to:
- Use the code for learning and academic reference  

However:
- It is not intended for production financial use  
- No guarantees are provided regarding correctness or compliance

---

## 👤 Author

**Henrique Santos Pereira**  
Computer Systems Engineering Student  

GitHub: https://github.com/hpereira07
