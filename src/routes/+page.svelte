<script lang="ts">
	import { SvelteFlow, Controls, Background, MiniMap, type Node, type Edge } from '@xyflow/svelte';
	import { FloatingLabelInput } from 'flowbite-svelte';

	import '@xyflow/svelte/dist/style.css';

	let nodes = $state.raw<Node[]>([
		{
			id: '1',
			data: { label: 'Hello' },
			position: { x: 0, y: 0 }
		},
		{
			id: '2',
			data: { label: 'World' },
			position: { x: 150, y: 150 }
		},
		{
			id: '3',
			data: { label: 'World' },
			position: { x: 150, y: 150 }
		}
	]);

	let edges = $state.raw<Edge[]>([
		{
			id: '1-2',
			source: '1',
			target: '2'
		}
	]);
</script>

<div id="exampleWrapper" class="grid w-full items-end gap-6 md:grid-cols-3">
	<FloatingLabelInput variant="filled" id="floating_filled" name="floating_filled" type="text"
		>Floating filled</FloatingLabelInput
	>
	<FloatingLabelInput variant="outlined" id="floating_outlined" name="floating_outlined" type="text"
		>Floating outlined</FloatingLabelInput
	>
	<FloatingLabelInput id="floating_standard" name="floating_standard" type="text"
		>Floating standard</FloatingLabelInput
	>
</div>

<div style:height="100vh">
	<SvelteFlow bind:nodes bind:edges fitView>
		<Controls />
		<Background />
		<MiniMap />
	</SvelteFlow>
</div>
