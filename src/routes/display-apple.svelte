<script lang="ts" context="module">
	export type AppleData = {
		type: "apple";
		name: string;
	};
</script>

<script lang="ts">
	const {data}:{data:AppleData} = $props()
</script>

<div style="color:green">
	<dt>🍏 {data.type}</dt>
	<dd>{data.name}</dd>
</div>