<script>
	import Person from './Person.svelte'
	
	export let item = {}
	
	const { location, people } = item
</script>

<section>
	<h2>{location}</h2>
	
	{#each people as person}
		<Person {person} />
	{/each}
</section>

<style>
	h2 {
		width: 100%;
		margin: 0 auto 2rem;
		font-size: 2.5em;
		text-align: center;
		color: #001668;
	}
	section {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		column-gap: 4rem;
		margin-bottom: 2rem;
	}
</style>