# How to Install Rust

Rust is a systems programming language focused on safety, speed, and concurrency. Follow the steps below to install Rust on your system.

---

## 📦 Installation (Recommended)

The recommended way to install Rust is via [`rustup`](https://rustup.rs), a tool for managing Rust versions.

### 🧰 Prerequisites
- Internet connection
- Terminal or command prompt access

---

## 🖥️ Windows

1. Download and run the rustup installer:
   [https://win.rustup.rs](https://win.rustup.rs)
2. Follow the on-screen instructions.
3. After installation, restart your terminal and run:
   ```sh
   rustc --version
   ```


🐧 Linux
---

1.Open your terminal.

2.Install Rust with:

```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
3.Follow the prompt to install.

4.Restart Terminal and check:
```sh
rustc --version
```

🧪 Verify Installation
After installing, you can check if everything works:
```sh
rustc --version
cargo --version
```

