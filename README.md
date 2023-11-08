# Initiation to Rust Programming Language

Welcome to the Initiation to Rust workshop! The objective of this workshop is to introduce you to the Rust programming language by covering its fundamentals. After completing this workshop, you can explore more advanced topics by referring to the official Rust documentation, which is a high-quality resource for learning Rust: [The Rust Programming Language](https://doc.rust-lang.org/book/title-page.html#the-rust-programming-language)

Rust is a multi-paradigm, general-purpose programming language that emphasizes performance, type safety, and concurrency. It enforces memory safety, meaning that all references point to valid memory, without requiring the use of automated memory management techniques such as garbage collection. To simultaneously enforce memory safety and prevent data races, its "borrow checker" tracks the object lifetime of all references in a program during compilation. Rust was influenced by ideas from functional programming, including immutability, higher-order functions, and algebraic data types. It is popular for systems programming.

You can learn more about memory management in Rust [here](https://doc.rust-lang.org/book/ch04-01-what-is-ownership.html)

## Step 00
* If you don't have it yet you will have to install curl:
```
sudo dnf -y install curl
```
* Begin by installing Rust on your system by typing the command below, more infos [here](https://www.rust-lang.org/tools/install)
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
* Once Rust is installed, you can initialize your Rust project using the Cargo tool. Cargo is Rust's package manager and build tool. You can find more information about Cargo in the official documentation [here](https://doc.rust-lang.org/cargo/getting-started/first-steps.html)
```
cargo new workshop_initiation
```

* Open your integrated development environment (IDE) of choice. Popular choices for Rust development include Visual Studio Code with the Rust extension, RustRover from JetBrains or Sumblime Text.

* Open the src/main.rs file in your IDE. This file contains the main Rust code for your project.

* You should see a simple "Hello, World!" example code in main.rs. It might look something like this:
```rust
fn main() {
    println!("Hello, World!");
}

```

* Open a terminal or command prompt and navigate to your project directory. You should be in the same directory as your Cargo.toml file, which is the project's configuration file.

* In the terminal, run the following command to build and execute your Rust code:
```
cargo run
```

**You will see the output "Hello, World!" in the terminal. Congratulations, you've successfully run your first Rust program!**

## Step 01
