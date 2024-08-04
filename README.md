// Generate a random number between 1 and 100
const randomNumber = Math.floor(Math.random() * 100) + 1;
let attempts = 0;
let guess = 0;

console.log("Welcome to the Number Guessing Game!");
console.log("I have generated a random number between 1 and 100.");

// Function to prompt the user for a guess
function guessNumber() {
    const userInput = prompt("Enter your guess:");
    guess = parseInt(userInput);
    attempts++;

    if (guess > randomNumber) {
        console.log("Your guess is too high.");
        guessNumber();
    } else if (guess < randomNumber) {
        console.log("Your guess is too low.");
        guessNumber();
    } else {
        console.log(Congratulations! You guessed the correct number ${randomNumber}.);
        console.log(It took you ${attempts} attempts.);
    }
}

// Start the game
guessNumber();
