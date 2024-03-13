<script lang="ts">
	import { AppBar, Avatar } from '@skeletonlabs/skeleton';
	import Popups from './Popups.svelte';
</script>

<AppBar gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">
	<svelte:fragment slot="lead">
		<Popups />
	</svelte:fragment>
	<svelte:fragment slot="trail">
		<Avatar width="w-10" initials="MK" background="bg-primary-500" />
	</svelte:fragment>
</AppBar>
