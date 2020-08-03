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

