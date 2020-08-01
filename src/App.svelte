<script>
	let count = 0;
  $:console.log(`the count is ${count}`)
	$:if(count>10){
		alert(`COUNT IS HIGH`);
		count =9
	}
	function handleClick() {
		count += 1;
	}
	
</script>

<button on:click={handleClick}>
	Clicked {count} {count === 1 ? 'time' : 'times'}
</button>

