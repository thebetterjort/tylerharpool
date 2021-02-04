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

I admit I've ever coded in C++/C. And to me, a garbage collector is something that happens every Thursday. Actually, that reminds me its trash day and I haven't taken out the trash.  Not learning C and C++ actually makes my path towards Rust seem all that much stranger to me. Especially given the references and the assumption that I should know how C++ handles things. 

For instance, The [Hello World](https://doc.rust-lang.org/stable/rust-by-example/macros.html) example on the Rust Website mentions `println!` is a macro. In order for us to create the hello world we should use this macro, but do not mistake it for a function because that would be wrong. Macros differ by the use of ! after the name. macro_rules!, printLn!.

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

This is basic enough. We have our main function, described as `fn main()` in Rust. The Rust Documentation says. "Rust provides a powerful macro system that allows metaprogramming." That is cool, but the benefits are not very apparent from looking at the code, and I don't know what metaprogramming is, or do I? I read Wikipedia and I found that being able to modify yourself even when running was a cool idea. Then I read Stack Overflow article on metaprogramming which one of the answers said I should read [Paul Graham's essay "What Made Lisp Different"](http://www.paulgraham.com/diff.html) and so I did. 

To be continued...
