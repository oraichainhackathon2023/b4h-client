<script>
	let name = '';
	$: greetMsg = `Hello ${name}`;
</script>

<div>
	<label class="label">
		<span>Input</span>
		<input class="input" type="text" placeholder="Enter a name.." bind:value={name} />
	</label>

	<button class="btn variant-filled-primary">Greet</button>
	<p>{greetMsg}</p>
</div>
