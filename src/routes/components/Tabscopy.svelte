<script context="module">
	export const TABS = {};
</script>

<script>
	import { setContext, onDestroy } from 'svelte';
	import { writable } from 'svelte/store';

	/**
	 * @type {any[]}
	 */
	const tabs = [];
	/**
	 * @type {any[]}
	 */
	const panels = [];
	const selectedTab = writable(null);
	const selectedPanel = writable(null);

	setContext(TABS, {
		registerTab: (/** @type {null} */ tab) => {
			tabs.push(tab);
			selectedTab.update(current => current || tab);
			
			onDestroy(() => {
				const i = tabs.indexOf(tab);
				tabs.splice(i, 1);
				selectedTab.update(current => current === tab ? (tabs[i] || tabs[tabs.length - 1]) : current);
			});
		},

		registerPanel: (/** @type {null} */ panel) => {
			panels.push(panel);
			selectedPanel.update(current => current || panel);
			
			onDestroy(() => {
				const i = panels.indexOf(panel);
				panels.splice(i, 1);
				selectedPanel.update(current => current === panel ? (panels[i] || panels[panels.length - 1]) : current);
			});
		},

		selectTab: (/** @type {null} */ tab) => {
			const i = tabs.indexOf(tab);
			selectedTab.set(tab);
			selectedPanel.set(panels[i]);
		},

		selectedTab,
		selectedPanel
	});
</script>

<div class="tabs ">
	<slot></slot>
</div>

<style>
    .tabs{
        width: 400px;
  height: 100%;
  display: flex;
  box-shadow: 0px 2px 4px rgba(119, 140, 163, 0.06),
  0px 4px 6px rgba(119, 140, 163, 0.1);
 border-radius: 8px;
 padding-top: 10px;


    }
</style>