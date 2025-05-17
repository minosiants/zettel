202503091301
Tags: #
__
# Idiomatic Rust

- In idiomatic Rust, functions do not take ownership of their arguments unless they need to
```rust
fn first_word(s: &String) -> ?
fn first_word(s: &str) -> &str //beter
```


__
### Zero-Links
- [[00-rust]]
- [[00-language]] 

__
### Links
- 

 
 