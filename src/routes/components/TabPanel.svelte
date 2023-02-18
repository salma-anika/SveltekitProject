<script>
	import { getContext } from 'svelte';
	import { TABS } from '../components/Tabscopy.svelte';

	const panel = {};
	const { registerPanel, selectedPanel } = getContext(TABS);

	registerPanel(panel);
</script>

{#if $selectedPanel === panel}
	<slot></slot>
{/if}