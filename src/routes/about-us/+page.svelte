<script lang="ts">
	import { fade, fly } from 'svelte/transition';
	import Square from '../../lib/components/Square.svelte';

	let titles = ['Hello', 'World', 'Foo', 'Bar'];
	let name = "";
	let show = false;
</script>

<div class="">
	<Square />
	<div class="text-8xl">HELLO</div>
	<form
		action=""
		on:submit={() => {
			show = true;
			setTimeout(() => {
				show = false;
			}, 1000);
		}}
		class="flex flex-col my-10 w-fit"
	>
		<label for="name">Name</label>
		<input type="text" id="name" bind:value={name} placeholder="enter your name" />
		<button type="submit" class="text-black">Sumbit</button>
	</form>
	<div class="hover:scale-125 transition-all duration-300">THing</div>
	{#if show}
		<div in:fade out:fly>{name}</div>
	{/if}
</div>
