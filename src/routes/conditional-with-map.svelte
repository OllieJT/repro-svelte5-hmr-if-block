<script lang="ts" context="module">
	export type FruitData = AppleData | OrangeData;
</script>

<script lang="ts">
	import DisplayApple, { type AppleData } from "./display-apple.svelte";
	import DisplayOrange, { type OrangeData } from "./display-orange.svelte";

	const {data}:{data:FruitData} = $props()

	const fruit_map = {
		"apple": DisplayApple,
		"orange": DisplayOrange
	} satisfies Record<FruitData["type"], ConstructorOfATypedSvelteComponent>
</script>

<svelte:component this={fruit_map[data.type]} data={data} />