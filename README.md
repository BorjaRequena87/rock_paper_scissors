Computer makes a choice and returns result
function computerPlay() {
    let choices = ['rock', 'paper', 'scissors'];
    let compChoice = Math.floor(Math.random() * 3);
    return choices[compChoice];
}

User makes a choice and returns result
function userPlay() {
    let userChoice;
    let choices = ['rock', 'paper', 'scissors'];
    while (!choices.includes(userChoice)) {
        userChoice = prompt("Rock, paper, or scissors?").toLowerCase();
    }
    return userChoice;
}

A single round
function playRound(userChoice, compChoice) {
    console.log("User: " + userChoice)
    console.log("Comp: " + compChoice)

    if (userChoice == compChoice) {
        return("Tie");
    } else if (userChoice == "rock" && compChoice == "scissors") ||
                userChoice == "paper" && compChoice == "rock" ||
                userChoice == "scissors" && compChoice == "paper") {
                    return("Win");
                } else {
                    return("Lose");
                }
}

Five rounds and return result


