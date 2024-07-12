<script lang="ts">
	import DisplayFruit, { type FruitData } from "./display-fruit.svelte";

	const fruits = $state<FruitData[]>([
		// List of sub-types of Fruit
		{ type: "apple", name: "Granny Smith" },
		{ type: "orange", name: "Mandarin" },
		{ type: "apple", name: "Fuji" },
		{ type: "orange", name: "Blood Orange" },

	])

</script>

{#each fruits as fruit}
	<DisplayFruit data={fruit} />
{/each}
