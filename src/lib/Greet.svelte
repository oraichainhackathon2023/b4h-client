<script>
	import { invoke } from '@tauri-apps/api/tauri';

	let name = '';
	let greetMsg = '';

	async function greet() {
		greetMsg = await invoke('greet', { name });
	}
</script>

<div>
	<input
		type="text"
		class="input input-bordered input-primary w-full max-w-xs"
		id="greet-input"
		placeholder="Enter a name..."
		bind:value={name}
	/>
	<button class="btn btn-primary" on:click={greet}>Greet</button>
	<p>{greetMsg}</p>
</div>
