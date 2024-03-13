<script lang="ts">
	import { AppBar } from '@skeletonlabs/skeleton';
	import PopMenu from './PopMenu.svelte';
</script>

<AppBar gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">
	<svelte:fragment slot="lead">
		<PopMenu />
	</svelte:fragment>
	<svelte:fragment slot="trail">(text)</svelte:fragment>
</AppBar>
