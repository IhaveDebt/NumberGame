<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Rock Paper Scissors Game</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 50px;
      background: #f0f0f0;
    }

    h1 {
      color: #333;
    }

    .choices {
      margin: 20px;
    }

    .choices button {
      font-size: 18px;
      padding: 10px 20px;
      margin: 10px;
      cursor: pointer;
      border: none;
      border-radius: 10px;
      background-color: #4CAF50;
      color: white;
      transition: background-color 0.3s ease;
    }

    .choices button:hover {
      background-color: #45a049;
    }

    #result {
      margin-top: 30px;
      font-size: 24px;
      color: #333;
    }

    #score {
      margin-top: 10px;
      font-size: 18px;
    }
  </style>
</head>
<body>

  <h1>Rock, Paper, Scissors ✊🖐✌️</h1>

  <div class="choices">
    <button onclick="play('rock')">Rock</button>
    <button onclick="play('paper')">Paper</button>
    <button onclick="play('scissors')">Scissors</button>
  </div>

  <div id="result">Make your choice!</div>
  <div id="score">You: 0 | Computer: 0</div>

  <script>
    let userScore = 0;
    let computerScore = 0;

    function play(userChoice) {
      const choices = ['rock', 'paper', 'scissors'];
      const computerChoice = choices[Math.floor(Math.random() * 3)];

      let result = '';

      if (userChoice === computerChoice) {
        result = "It's a draw! 😐";
      } else if (
        (userChoice === 'rock' && computerChoice === 'scissors') ||
        (userChoice === 'paper' && computerChoice === 'rock') ||
        (userChoice === 'scissors' && computerChoice === 'paper')
      ) {
        result = `You win! 🎉 ${userChoice} beats ${computerChoice}`;
        userScore++;
      } else {
        result = `You lose! 😢 ${computerChoice} beats ${userChoice}`;
        computerScore++;
      }

      document.getElementById('result').innerText = result;
      document.getElementById('score').innerText = `You: ${userScore} | Computer: ${computerScore}`;
    }
  </script>

</body>
</html>

            print("❌ Please enter a valid number.")

if __name__ == "__main__":
    main()
