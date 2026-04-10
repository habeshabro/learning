#rust #lowlevel #basic 
**Key Concepts**

### Toolchain
- rustup: to install and manage rust
- rust-std: standard rust library
- cargo: package manager
- clippy
- rust-docs: offline documentation
- rustc: compiler


## Hello world

```rust
fn main() {
	println!("Hello World");
}
```
rustc to compile


## Cargo

```sh
# to make new project
cargo new hello_cargo
# to build the project
cargo build
#to compile then run the project
cargo run
#to check if the code is viable without building
cargo check
#to build for deployment
cargo build --release
#to open documentation
cargo doc --open 
```

    
