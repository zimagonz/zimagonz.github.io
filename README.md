# HI CASSIE
WELCOME TO MY QUIZ
[Uploading c<html>
<head>
<title>cass-quiz.html</title>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
<style type="text/css">
.s0 { color: #d5b778;}
.s1 { color: #bcbec4;}
.s2 { color: #bababa;}
.s3 { color: #6aab73;}
</style>
</head>
<body bgcolor="#1e1f22">
<table CELLSPACING=0 CELLPADDING=5 COLS=1 WIDTH="100%" BGCOLOR="#606060" >
<tr><td><center>
<font face="Arial, Helvetica" color="#000000">
cass-quiz.html</font>
</center></td></tr></table>
<pre><span class="s0">&lt;!DOCTYPE </span><span class="s2">html</span><span class="s0">&gt;</span>
<span class="s0">&lt;html </span><span class="s2">lang</span><span class="s3">=&quot;en&quot;</span><span class="s0">&gt;</span>
<span class="s0">&lt;head&gt;</span>
    <span class="s0">&lt;meta </span><span class="s2">charset</span><span class="s3">=&quot;UTF-8&quot;</span><span class="s0">&gt;</span>
    <span class="s0">&lt;meta </span><span class="s2">name</span><span class="s3">=&quot;viewport&quot; </span><span class="s2">content</span><span class="s3">=&quot;width=device-width, initial-scale=1.0&quot;</span><span class="s0">&gt;</span>
    <span class="s0">&lt;title&gt;</span><span class="s1">Boyfriend Quiz</span><span class="s0">&lt;/title&gt;</span>
    <span class="s0">&lt;style&gt;</span>
        <span class="s1">body {</span>
            <span class="s1">font-family: Arial, sans-serif;</span>
            <span class="s1">margin: 20px;</span>
            <span class="s1">padding: 0;</span>
            <span class="s1">text-align: center;</span>
        <span class="s1">}</span>
        <span class="s1">.container {</span>
            <span class="s1">max-width: 600px;</span>
            <span class="s1">margin: 0 auto;</span>
        <span class="s1">}</span>
        <span class="s1">.question {</span>
            <span class="s1">margin: 20px 0;</span>
        <span class="s1">}</span>
        <span class="s1">button {</span>
            <span class="s1">margin-top: 10px;</span>
            <span class="s1">padding: 10px 20px;</span>
            <span class="s1">font-size: 16px;</span>
            <span class="s1">cursor: pointer;</span>
        <span class="s1">}</span>
    <span class="s0">&lt;/style&gt;</span>
<span class="s0">&lt;/head&gt;</span>
<span class="s0">&lt;body&gt;</span>
    <span class="s0">&lt;div </span><span class="s2">class</span><span class="s3">=&quot;container&quot;</span><span class="s0">&gt;</span>
        <span class="s0">&lt;h1&gt;</span><span class="s1">Welcome to the Boyfriend Quiz!</span><span class="s0">&lt;/h1&gt;</span>
        <span class="s0">&lt;div </span><span class="s2">id</span><span class="s3">=&quot;quiz&quot;</span><span class="s0">&gt;</span>
            <span class="s0">&lt;div </span><span class="s2">id</span><span class="s3">=&quot;question-container&quot; </span><span class="s2">class</span><span class="s3">=&quot;question&quot;</span><span class="s0">&gt;</span>
                <span class="s0">&lt;p </span><span class="s2">id</span><span class="s3">=&quot;question&quot;</span><span class="s0">&gt;&lt;/p&gt;</span>
                <span class="s0">&lt;input </span><span class="s2">type</span><span class="s3">=&quot;text&quot; </span><span class="s2">id</span><span class="s3">=&quot;answer&quot; </span><span class="s2">placeholder</span><span class="s3">=&quot;Your answer&quot;</span><span class="s0">&gt;</span>
            <span class="s0">&lt;/div&gt;</span>
            <span class="s0">&lt;button </span><span class="s2">id</span><span class="s3">=&quot;next-button&quot; </span><span class="s2">onclick</span><span class="s3">=&quot;nextQuestion()&quot;</span><span class="s0">&gt;</span><span class="s1">Next</span><span class="s0">&lt;/button&gt;</span>
        <span class="s0">&lt;/div&gt;</span>
        <span class="s0">&lt;div </span><span class="s2">id</span><span class="s3">=&quot;result&quot; </span><span class="s2">class</span><span class="s3">=&quot;question&quot; </span><span class="s2">style</span><span class="s3">=&quot;display: none;&quot;</span><span class="s0">&gt;</span>
            <span class="s0">&lt;p </span><span class="s2">id</span><span class="s3">=&quot;score&quot;</span><span class="s0">&gt;&lt;/p&gt;</span>
            <span class="s0">&lt;button </span><span class="s2">onclick</span><span class="s3">=&quot;restartQuiz()&quot;</span><span class="s0">&gt;</span><span class="s1">Restart Quiz</span><span class="s0">&lt;/button&gt;</span>
        <span class="s0">&lt;/div&gt;</span>
    <span class="s0">&lt;/div&gt;</span>

    <span class="s0">&lt;script&gt;</span>
        <span class="s1">const questions = [</span>
            <span class="s1">{ question: &quot;Where was I born?&quot;, answer: &quot;midland&quot; },</span>
            <span class="s1">{ question: &quot;What's the first name of my favorite artist of all time?&quot;, answer: &quot;kanye&quot; },</span>
            <span class="s1">{ question: &quot;What's the 3rd song on BWH?&quot;, answer: &quot;so lovely&quot; },</span>
            <span class="s1">{ question: &quot;What's my favorite candy right now?&quot;, answer: &quot;sweet tarts&quot; },</span>
            <span class="s1">{ question: &quot;What music do I like right now in life?&quot;, answer: &quot;classical&quot; }</span>
        <span class="s1">];</span>

        <span class="s1">let currentQuestion = 0;</span>
        <span class="s1">let score = 0;</span>

        <span class="s1">function nextQuestion() {</span>
            <span class="s1">const userAnswer = document.getElementById('answer').value.trim().toLowerCase();</span>
            <span class="s1">if (userAnswer === questions[currentQuestion].answer) {</span>
                <span class="s1">score++;</span>
            <span class="s1">}</span>
            <span class="s1">currentQuestion++;</span>
            <span class="s1">if (currentQuestion &lt; questions.length) {</span>
                <span class="s1">showQuestion();</span>
            <span class="s1">} else {</span>
                <span class="s1">showResult();</span>
            <span class="s1">}</span>
        <span class="s1">}</span>

        <span class="s1">function showQuestion() {</span>
            <span class="s1">document.getElementById('question').textContent = questions[currentQuestion].question;</span>
            <span class="s1">document.getElementById('answer').value = '';</span>
        <span class="s1">}</span>

        <span class="s1">function showResult() {</span>
            <span class="s1">document.getElementById('quiz').style.display = 'none';</span>
            <span class="s1">document.getElementById('result').style.display = 'block';</span>
            <span class="s1">document.getElementById('score').textContent = `You got ${score} out of ${questions.length} questions correct!`;</span>
        <span class="s1">}</span>

        <span class="s1">function restartQuiz() {</span>
            <span class="s1">currentQuestion = 0;</span>
            <span class="s1">score = 0;</span>
            <span class="s1">document.getElementById('result').style.display = 'none';</span>
            <span class="s1">document.getElementById('quiz').style.display = 'block';</span>
            <span class="s1">showQuestion();</span>
        <span class="s1">}</span>

        <span class="s1">// Start the quiz by showing the first question</span>
        <span class="s1">showQuestion();</span>
    <span class="s0">&lt;/script&gt;</span>
<span class="s0">&lt;/body&gt;</span>
<span class="s0">&lt;/html&gt;</span>
</pre>
</body>
</html>ass-quiz.html.html…]()
