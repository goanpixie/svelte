<script>
	let count = 0;

	function handleClick(){
		count++
	}
</script>

<button on:click={handleClick}>
	Cliked {count}{count===1 ? "time" : "times"}
</button>

