202407132041
Tags: #rust
__
# Rust
## Concepts
### Ownership 

```rust
	let str1 = String::from("hello world");
	let str2 = str1;
	print!(str1); // will not compile
```

### Borrowing

immutable borrowing
```rust
let str1 = String::from("hello");
let only_ascii = only_ascii(&str1);
if only_ascii {
	println!("No unicode");
}
fn only_ascii(s: &String) -> bool {
	s.is_ascii()
}
```

mutable borrowing 
```rust
let str1 = String::from("hello");
append_world(&str1)
println!(str1);
fn append_world(s: &mut String){
	str1.push_str(" world");
}
```

lifetime
Rust borrow checker uses lifetimes to prevent dangling references, which occur when a reference outlive the data it refers to. 
```rust
let str1 = String::from("hello");
let str2 = String::from("world");
let result = find_longest(&str1, &str2);
//'a helps to understand compiler that both references can be returned
fn find_logest<'a>(str1: &'a String, str2: &'a String)-> &'a String {
	use::std::cmp:Ordering::*
	match str1.len().comp(str2.len) {
		Greater => &str1,
		Equal => "",
		Less => &str2,
		
	}
}
```

[full example](https://play.rust-lang.org/?version=stable&mode=debug&edition=2021&gist=b600bd45c2e3ff5bf51b177692395ae6)
### Smart Pointers

```rust
let data = Box:new([0; 1024*1024]);
println(data.len());
```


### Resources
- ### [Reference](https://doc.rust-lang.org/reference/introduction.html)
* ### [cheatsheet](https://upsuper.github.io/rust-cheatsheet/?dark,single,large)
- [build-your-own-jira-with-rust](https://github.com/LukeMathWalker/build-your-own-jira-with-rust)
- [idiomatic rust](https://github.com/mre/idiomatic-rust) 
- [google course](https://github.com/google/comprehensive-rust) 
- [elegant api in rust](https://deterministic.space/elegant-apis-in-rust.html)
- https://rust-lang.github.io/async-book/
- https://github.com/tokio-rs/mini-redis/
* https://programming-idioms.org/cheatsheet/Rust
* [Achieving warp speed with Rust](https://gist.github.com/jFransham/369a86eff00e5f280ed25121454acec1)
* [awesome-rust](https://github.com/rust-unofficial/awesome-rust)
* [design patterns](https://rust-unofficial.github.io/patterns/)


 - [auto-currying_rust_functions](https://oppi.li/posts/auto-currying_rust_functions/)
### Zero-Links`
- [[00-language]]

__
### Links
- 

 
