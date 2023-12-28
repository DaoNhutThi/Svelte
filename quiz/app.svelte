<script>
	import Answer from "./Answer.svelte";
	import Question from "./Question.svelte";
	import Point from "./Point.svelte";

	let points = 0;
	let quizIndex = 0;
	const quiz= [
		{
			question: 'Is there any tea in the cup?', 
			correctAnswer:0,
			answer: [
				'yes',
				'no'
			]
		},
		{
			question: 'Is there a bike in front of my house?',
			correctAnswer:0,
			answer: [
				'yes',
				'no'
			]
		},
		{
			question: 'Are there many students in the school?',
			correctAnswer:0,
			answer: [
				'yes',
				'no'
			]
		}, 
		{
			question: 'Is there any tea in the cup?',
			correctAnswer:0,
			answer: [
				'yes',
				'no'
			]
		}
	]
	function checkAnswerHandler(answerText) {
		const isCorrect = quiz[quizIndex].answer.indexOf(answerText) ===
			quiz[quizIndex].correctAnswer;
		if (isCorrect)
		{
			// points += 1;
			quiz[quizIndex].question = "correct!"
			alert('chuc mung') 
		} else 
		{
			quiz[quizIndex].question = "incorrect!"
			alert('sorry')
		} setTimeout(function () {
                    quizIndex += 1;
                }, 2000);
	}
	</script>
<Point point = {points}/>
<Question questionText={quiz[quizIndex].question}/>
<Answer answerText={quiz[quizIndex].answer[0]} checkAnswerHandler={checkAnswerHandler}/>
<Answer answerText={quiz[quizIndex].answer[1]} checkAnswerHandler={checkAnswerHandler}/>


