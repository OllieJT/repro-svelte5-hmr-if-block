<script lang="ts" context="module">
	export type FruitData = AppleData | OrangeData;
</script>

<script lang="ts">
	import DisplayApple, { type AppleData } from "./display-apple.svelte";
	import DisplayOrange, { type OrangeData } from "./display-orange.svelte";

	const {data}:{data:FruitData} = $props()
</script>

{#if data.type === "apple"}
	<DisplayApple {data} />
{:else if data.type === "orange"}
	<DisplayOrange {data} />
{/if}