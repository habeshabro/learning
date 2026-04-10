#rust #basic 
###  Guessing Game Project

first iteration
```rust
use rand::Rng;
use std::io;
use std::cmp::Ordering;


fn random_number() -> u32 {
    rand::thread_rng().gen_range(1..=100)
}
// fn string_to_u32(s: &str) -> Option<u32> {
//     match s.trim().parse::<u32>() {
//         Ok(num) => Some(num),
//         Err(_) => None,
//     }
// }

fn main() {
    let secret_number = random_number();
    println!("Guess the number!");
    loop {
        let mut guess = String::new(); //mut means mutable variable, :: associated function
        println!("Please input your guess.");
        io::stdin()
            .read_line(&mut guess) //& passed by reference to avoid taking ownership, mut to allow modification, returns Result type
            .expect("failed to read line"); // if error variant occurs, crash program and display message,
        println!("You guessed: {guess}");

        let guess: u32 = match guess.trim().parse() {
            Ok(num) => num,
            Err(_) => {
                println!("Please enter a valid number!");
                continue;
            }
        };

        match guess.cmp(&secret_number) {
            Ordering::Less => println!("Too small!"),
            Ordering::Greater => println!("Too big!"),
            Ordering::Equal => {
                println!("You win!");
                break;
            },
        }
    }

}
```


