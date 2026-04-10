#rust #basic 
```rust
fn main() {
	let mut x = 5; //if mut is missing, then it becomes immutable
	println!("The value of x is {x}");
	x = 6;
	println!("The value of x is now {x}");
}
```

constants must be known at compile time. e.g. the size of an array must be constant.

A const fn must be evaluable at compile time if it's arguments are.

Immutable variables don't have this restriction, they only state you can't get a unique (mutable) reference to the variable.

shadowing is "overshadowing" the existing variable with a new one, and that one is the one that will be visible in that scope

```rust 
fn main() {
	let x = 5;
	let x = x + 1;
	{
		let x = x * 2 ;
		println!("in the inner scope, x is {x}"); // prints out 12
	}
	println!("but out here, it is still {x}"); // prints out 6
}
```

when we use shadowing, we are creating a brand new variable so types don't matter

## Scalar Types
- integers
- floating point types 
- Booleans
- chars
- 