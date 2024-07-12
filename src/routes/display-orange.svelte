<script lang="ts" context="module">
	export type OrangeData = {
		type: "orange";
		name: string;
	};
</script>

<script lang="ts">
	const {data}:{data:OrangeData} = $props()
</script>

<div style="color:orange">
	<dt>🍊 {data.type}</dt>
	<dd>{data.name}</dd>
</div>