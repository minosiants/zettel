202505191337
Tags: #lifetime
__
# Rust Lifetime

#### [common-rust-lifetime-misconceptions](https://github.com/pretzelhammer/rust-blog/blob/master/posts/common-rust-lifetime-misconceptions.md)
In a nutshell: A variable's lifetime is how long the data it points to can be statically verified by the compiler to be valid at its current memory address.

- `T` is a superset of both `&T` and `&mut T`
- `&T` and `&mut T` are disjoint sets
- `T: 'static` should be read as _"`T` can live at least as long as a `'static` lifetime"_
- if `T: 'static` then `T` can be a borrowed type with a `'static` lifetime _or_ an owned type
- since `T: 'static` includes owned types that means `T`
    - can be dynamically allocated at run-time
    - does not have to be valid for the entire program
    - can be safely and freely mutated
    - can be dynamically dropped at run-time
    - can have lifetimes of different durations
- `T: 'a` is more general and more flexible than `&'a T`
- `T: 'a` accepts owned types, owned types which contain references, and references
- `&'a T` only accepts references
- if `T: 'static` then `T: 'a` since `'static` >= `'a` for all `'a`
- almost all Rust code is generic code and there's elided lifetime annotations everywhere
- Rust's lifetime elision rules are not always right for every situation
- Rust does not know more about the semantics of your program than you do
- give your lifetime annotations descriptive names
- try to be mindful of where you place explicit lifetime annotations and why
- all trait objects have some inferred default lifetime bounds
- Rust compiler error messages suggest fixes which will make your program compile which is not that same as fixes which will make you program compile _and_ best suit the requirements of your program
- lifetimes are statically verified at compile-time
- lifetimes cannot grow or shrink or change in any way at run-time
- Rust borrow checker will always choose the shortest possible lifetime for a variable assuming all code paths can be taken
- try not to re-borrow mut refs as shared refs, or you're gonna have a bad time
- re-borrowing a mut ref doesn't end its lifetime, even if the ref is dropped
- every language has gotchas 🤷


__
### Zero-Links
- [[00-rust]]

__
### Links
- 

 
 