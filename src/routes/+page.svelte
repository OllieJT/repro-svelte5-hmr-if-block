<script lang="ts">
	import ConditionalWithIf, { type FruitData } from "./conditional-with-if.svelte";
	import ConditionalWithMap from "./conditional-with-map.svelte";

	const fruits = $state<FruitData[]>([
		// List of sub-types of Fruit
		{ type: "apple", name: "Granny Smith" },
		{ type: "orange", name: "Mandarin" },
		{ type: "apple", name: "Fuji" },
		{ type: "orange", name: "Blood Orange" },
	])

</script>

<h2>If Block</h2>
<p>This uses an if block to conditionally render a component.</p>
<dl>
	{#each fruits as fruit}
	<ConditionalWithIf data={fruit} />
	{/each}
</dl>

<hr />

<h2>Component Map</h2>
<p>This uses a component map and svelte:component element to conditionally render a component.</p>
<dl>
	{#each fruits as fruit}
	<ConditionalWithMap data={fruit} />
	{/each}
</dl>
