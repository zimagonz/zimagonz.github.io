# cass-quiz
print("I hope this quiz works"
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Boyfriend Quiz</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            padding: 0;
            text-align: center;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
        }
        .question {
            margin: 20px 0;
        }
        button {
            margin-top: 10px;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Welcome to the Boyfriend Quiz!</h1>
        <div id="quiz">
            <div id="question-container" class="question">
                <p id="question"></p>
                <input type="text" id="answer" placeholder="Your answer">
            </div>
            <button id="next-button" onclick="nextQuestion()">Next</button>
        </div>
        <div id="result" class="question" style="display: none;">
            <p id="score"></p>
            <button onclick="restartQuiz()">Restart Quiz</button>
        </div>
    </div>

    <script>
        const questions = [
            { question: "Where was I born?", answer: "midland" },
            { question: "What's the first name of my favorite artist of all time?", answer: "kanye" },
            { question: "What's the 3rd song on BWH?", answer: "so lovely" },
            { question: "What's my favorite candy right now?", answer: "sweet tarts" },
            { question: "What music do I like right now in life?", answer: "classical" }
        ];

        let currentQuestion = 0;
        let score = 0;

        function nextQuestion() {
            const userAnswer = document.getElementById('answer').value.trim().toLowerCase();
            if (userAnswer === questions[currentQuestion].answer) {
                score++;
            }
            currentQuestion++;
            if (currentQuestion < questions.length) {
                showQuestion();
            } else {
                showResult();
            }
        }

        function showQuestion() {
            document.getElementById('question').textContent = questions[currentQuestion].question;
            document.getElementById('answer').value = '';
        }

        function showResult() {
            document.getElementById('quiz').style.display = 'none';
            document.getElementById('result').style.display = 'block';
            document.getElementById('score').textContent = `You got ${score} out of ${questions.length} questions correct!`;
        }

        function restartQuiz() {
            currentQuestion = 0;
            score = 0;
            document.getElementById('result').style.display = 'none';
            document.getElementById('quiz').style.display = 'block';
            showQuestion();
        }

        // Start the quiz by showing the first question
        showQuestion();
    </script>
</body>
</html>
