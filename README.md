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

* Open your integrated development environment (IDE) of choice. Popular choices for Rust development include Visual Studio Code with the Rust extension, RustRover from JetBrains or Sumblime Text.


## Step 01

* For now we will start with the basics and create a simple Hello World function.

* Start creating  the "hello_world" folder, inside you can add main.rs file

* You can now type the code below to create your first function in Rust:
```rust
fn main() {
    println!("Hello, World!");
}

```

* Open a terminal or command prompt and navigate to your project directory. You should be in the same directory as your Cargo.toml file, which is the project's configuration file.

* In the terminal, run the following command to build and execute your Rust code:
```
rustc main.rs
```

**You will see the output "Hello, World!" in the terminal. Congratulations, you've successfully run your first Rust program!**

## Step 02

In this step, you will learn more about Variable and Data Types

**It is obvious that Rust allows you to declare all you're variable without adding the optional type annotations, however for this step i would like you to use the type annotations for all your declarations and it still is a good practice to avoid easy mistakes related to types...**

* First I will ask you to create several variables, you should choose the according type depending of each cases:
  - i: integer type, assigned value of `42`
  - j: integer type, assigned value of `32421`
  - k: integer type, assigned value of `-75000`
  - f: floating-point type, assigned value of `3.14159`
  - t: tuple of integers, assigned value of  `i, j, k, f`
  - a: array of strings, assigned value of `"This", "Was", "A", "Good", "Day"`
  - HELLO_WORLD: const string type,  assigned value of `Hello World 😁`

> if you need informations about Rust Data Types don't forget to check the [Book](https://doc.rust-lang.org/book/ch03-02-data-types.html)
 
* After declaring all your variables you can add these lines of code at the end of your function to check if everything matches:

```rust
println!("i = {}", i);
println!("j = {}", j);
println!("k = {}", k);
println!("f = {}", f);
println!("t = {:?}", t);
println!("a = {:?}", a);
println!("HELLO_WORLD = {}", HELLO_WORLD);
```

## Step 03

In this step you will learn more about functions. You have to keep your previous variables.

**Just like before i will ask you to precise return types in all your functions**

I believe the name of the functions are pretty self-explanatory, so i'll let you implement them.

```rust
println!("{}",add(i, j));
println!("{}", sub(k, f));
display(t);

let a: [&str; 4] = pop(a);
println!("{:?} ",a);
```

> If you're observant, you might be wondering why you can redeclare the same function 'a' in this scope. Congratulations on your attentiveness! If you're interested, you can learn more about the concept of shadowing by clicking [here](https://doc.rust-lang.org/book/ch03-01-variables-and-mutability.html#shadowing) 

Expected OUTPUT:
```
32463
-75003.14
42 32421 -75000 3.14159
["This", "Was", "A", "Good"] 
```

## Informations about mutability of the variables

After you've completed your code, add the following line:
```
i = i + 1;
```

If you tried to compile your program and encountered an issue, you just witnessed something we haven't discussed yet. In Rust, by default, variables are immutable. This is one of the ways Rust encourages writing code that is safe and suitable for concurrency. However, you still have the option to make your variables mutable.

Make your variable "i" mutable and try compiling your code again

You can find more information about variables and mutability [here](https://doc.rust-lang.org/book/ch03-01-variables-and-mutability.html#variables-and-mutability)

## Step 04

> Tip: Create a new folder with a new main file for this step.

In this step let's delve into [contol flow](https://doc.rust-lang.org/book/ch03-05-control-flow.html)

We previously overlooked a type `bool`. Without delving too deep into details, 
In most programming languages, including Rust, the `bool` type is fundamental to control flow. 
It represents boolean values, namely `true` or `false`. Boolean values are pivotal in decision-making processes within programs. **Conditions**, **loops**, and various control structures often rely on boolean expressions to determine the flow of execution.


### Conditions

Implement your main to produce the following output:

OUTPUT
```
42 is even
89 number is not divisible by 4, 3, or 2
32 number is divisible by 4
30 number is divisible by 3
10 number is divisible by 2
```

> Don't forget to create functions to avoid repeating code.

### Loops

For the loop part, you'll be tasked with three different loops. We'll exclude the while loop since it functions as you already know.

* Loop with a Break:
    - Initialize a mutable variable `n` to 0.
    - Use a loop to increment `n` until it reaches 42.
    - When `n` equals 42, break out of the loop and set `result` to `n` * 2.
    - Print the `result`.

* Iterate Over an Array:
    - Create an array with values: [10, 20, 30, 40, 50].
    - Utilize a loop to iterate over each element in the array.
    - Print each element.

* Range Loop:
    - Use a loop to iterate over numbers from 1 to 9 (inclusive).
    - Print each number in the loop.


```
result = 84
the value is: 10
the value is: 20
the value is: 30
the value is: 40
the value is: 50
range: 1
range: 2
range: 3
range: 4
range: 5
range: 6
range: 7
range: 8
range: 9
```

## Step 05

In this step we will learn about struct.

I will slowly stop givin you pieces of code, so far you should be able to make it all by yourself

### Declare User Struct

Create `User` struct containing those pieces of data: 
* firstname,
* lastname,
* age,
* email,
* city,
* enabled,
* uid

Match this output:
```
User: John Doe is 32 from New York, [ email: john.doe@mail.com, account is enabled: true, uid: 123456 ]
```

### Declare Rgb tuple Struct

Now declare green, red, blue, black and white using `Rgb tuple struct type` and assigning correct values

### Declare Circle Struct and Implement Methods

* Declare `Circle` Struct:
    * The `Circle` struct should contain a single piece of data, the `radius`. Use the most appropriate and precise type for the radius.

* Implement Methods for Circle Struct:
    * `area`: Return the area of the circle.
    * `perimeter`: Return the perimeter of the circle.
    * `grow`: Allow the user to increment the size of the circle.
    * `is_larger`: Return a boolean indicating if the radius of one circle is larger than another.

**To verify this functionality, perform the following actions:**

* Declare `circle0` with a radius of 2.
* Declare `circle1` with a radius of 3.
* Increase the `radius` of `circle0` by 2 units.

The expected output should be as follows:

```
Circle0 area: 12.566370614359172
Circle0 perimeter: 12.566370614359172
Circle1 area: 28.274333882308138
Circle1 perimeter: 18.84955592153876

Circle0 area after grow: 50.26548245743669
Circle0 perimeter after grow: 25.132741228718345
Is circle0 larger than circle1 ? true
```

## That's the culmination of your initiation into Rust! If you're keen on exploring further, I suggest diving into topics like [enum](https://doc.rust-lang.org/book/ch06-00-enums.html) and [ownership](https://doc.rust-lang.org/book/ch04-00-understanding-ownership.html) for more intriguing concepts in Rust programming.

