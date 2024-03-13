<script lang="ts">
	import { AppBar } from '@skeletonlabs/skeleton';
	import Popups from './Popups.svelte';
</script>

<AppBar gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">
	<svelte:fragment slot="lead">
		<Popups />
	</svelte:fragment>
	<svelte:fragment slot="trail">(text)</svelte:fragment>
</AppBar>
