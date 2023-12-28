<script>
	export let answerText;
	export let checkAnswerHandler;
</script>
<button on:click={()=> checkAnswerHandler(answerText)}>
	{answerText}
</button>