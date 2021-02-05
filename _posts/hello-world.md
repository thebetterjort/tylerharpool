---
title: 'Learn Rust: Macros'
excerpt: 'The first thing I noticed when writing the hello world app is that Macros seemed to be something important.'
coverImage: '/assets/blog/hello-world/cover.jpg'
date: '2021-02-03T05:35:07.322Z'
author:
  name: Tyler Harpool
  picture: '/assets/blog/authors/tyler.jpeg'
ogImage:
  url: '/assets/blog/hello-world/cover.jpg'
---


## Macros

The [Hello World](https://doc.rust-lang.org/stable/rust-by-example/macros.html) example on the [Rust Website](https://rust-lang.org) mentions `println!` outputs the text to the terminal. For us to create the `hello world` application in Rust we should use this highly efficient [macro](https://doc.rust-lang.org/stable/rust-by-example/macros.html), but do not mistake it for a function because that would be wrong. `Macros` differ to `fn` by the use of `!` after the constant. 

We can see: `macro_rules!`, `printLn!` in the code below:
The Rust people, want you to remember that using Macros is highly efficient because its not a string like you would find in C, but a Abstract Syntax Tree, so you will not get as many bugs. 

Here is the basic `Hello World` app:

```
// This is a simple macro named `say_hello`.
macro_rules! say_hello {
    // `()` indicates that the macro takes no argument.
    () => {
        // The macro will expand into the contents of this block.
        println!("Hello!");
    };
}

fn main() {
    // This call will expand into `println!("Hello");`
    say_hello!()
}

```

This example is basic enough. We have a main function that we define as `fn main()`. The [Rust Documentation](https://doc.rust-lang.org/beta/book/index.html) says, "Rust provides a powerful macro system that allows [metaprogramming](https://en.wikipedia.org/wiki/Metaprogramming)." That is cool, but the benefits are not very apparent from looking at the code, and I don't know what [metaprogramming](https://en.wikipedia.org/wiki/Metaprogramming) is, or do I? I read [Wikipedia](https://en.wikipedia.org/wiki/Metaprogramming) and my initial reaction is that being able to modify your app even when its still running sounds cool. Then I read this [Stack Overflow](https://stackoverflow.com/a/514697/562312) article on what metaprogramming was. The answer I found interesting said I should read [Paul Graham's essay "What Made Lisp Different"](http://www.paulgraham.com/diff.html) and so I did. 

## Conclusion
* Macros can be described as "writing code that writes code"

## Questions
* How do we build new Macros? 
* What are `Macros` benefits over `fn`?

# Next
* Rust feels so primative. (Coming soon...)



