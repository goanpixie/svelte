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

	let user = { loggedIn: false };

	function toggle() {
		user.loggedIn = !user.loggedIn;
	}

	let x=9;
</script>

<button on:click={handleClick}>
	Clicked {count} {count === 1 ? 'time' : 'times'}
</button>

{#if user.loggedIn}
	<button on:click={toggle}>
		Log out
	</button>
{:else}
	<button on:click={toggle}>
		Log in
	</button>
{/if}

{#if x > 10}
	<p>{x} is greater than 10</p>
{:else}
	{#if 5 > x}
		<p>{x} is less than 5</p>
	{:else}
		<p>{x} is between 5 and 10</p>
	{/if}
{/if}

