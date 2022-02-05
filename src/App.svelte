<script>
	import { data } from './data.js'
	import Location from './Location.svelte'
</script>

<main>
	{#each data as item}
		<Location {item} />
	{/each}
</main>