<!DOCTYPE html>
<html>
<head>
  <title>Page Title</title>
  <meta charset="UTF-8"/>
</head>
<body>

  <p></p>

  <script>
    const para = document.querySelector('p');

    function computerPlay() {
        let compArray = ['rock', 'paper', 'scissors'];
        let randNew = compArray[Math.floor(Math.random()*compArray.length)];
        return randNew;
    }
    function playRound(playerSelection, computerSelection) {
        if (playerSelection == 'rock' & computerSelection == 'paper') {
          console.log("You lose! Paper beats rock.");
          return pc++;
        } else if (playerSelection == 'rock' & computerSelection == 'scissors') {
          console.log("You win! Rock beats scissors.");
          return user++;
        } else if (playerSelection == 'scissors' & computerSelection == 'paper') {
          console.log("You win! Scissors beat paper.");
          return user++;
        } else if (playerSelection == 'paper' & computerSelection == 'rock') {
          console.log("You win! Paper beats rock.");
          return user++;
        } else if (playerSelection == 'paper' & computerSelection == 'scissors') {
          console.log("You lose! Scissors beats paper,");
          return pc++;
        } else if (playerSelection == 'scissors' & computerSelection == 'rock') {
          console.log("You lose! rock beats scissors.");
          return pc++
        } else if (playerSelection == computerSelection) { 
          console.log("It is a draw!");
          return tie++;
        } else {
          console.log("Get outta here with that BS.");
          return null;
          }
        }

    function game() {
      match = 0;
        while(match!=5)
        {
         computerSelection = computerPlay();
         playerSelection = prompt("Rock, Paper, or Scissors?").toLowerCase();
         console.log(playRound(playerSelection, computerSelection));
         match++;
        }

        if (user > pc) {
          para.textContent = "You win.";
          return "You win.";
        } else if (pc > user){
          para.textContent = "You lose.";
          return "You lose.";
        } else {
          para.textContent = "A draw!"
          return "Draw.";
        }

        
     }

    let user = 0;
    let pc = 0;
    let tie = 0;

    

    game();
  </script>
</body>
</html>