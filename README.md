# quizz-game-using-js
// 1. Predefined set of questions and answers
const quiz = [
  { question: "What is the capital of France?", answer: "paris" },
  { question: "What planet is known as the Red Planet?", answer: "mars" },
  { question: "What is the largest ocean on Earth?", answer: "pacific" },
  { question: "What gas do plants breathe in?", answer: "carbon dioxide" }
];

// 2. Function to run the quiz
function startQuiz() {
  let score = 0; // Track score

  for (let i = 0; i < quiz.length; i++) {
    const userInput = prompt(quiz[i].question);

    // If user cancels, break out
    if (userInput === null) {
      alert("Quiz canceled.");
      return;
    }

    const cleanedInput = userInput.trim().toLowerCase();

    if (cleanedInput === quiz[i].answer) {
      alert("Correct!");
      score++;
    } else {
      alert("Incorrect. The correct answer was: " + quiz[i].answer);
    }
  }

  // 3. Final score output
  alert("Quiz complete! Your final score is " + score + " out of " + quiz.length);
}

// 4. Start the quiz
startQuiz();
