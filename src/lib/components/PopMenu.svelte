<script lang="ts">
	import { popup, LightSwitch } from '@skeletonlabs/skeleton';
	import type { PopupSettings } from '@skeletonlabs/skeleton';

	const popupClick: PopupSettings = {
		event: 'click',
		target: 'popupClick',
		placement: 'bottom',
		closeQuery: '.btn'
	};
</script>

<button class="btn bg-primary-hover-token variant-filled-900" use:popup={popupClick}>
	<div class="flex items-center justify-center gap-1">
		<span class="flex items-center">Explore</span>
		<svg
			fill="currentColor"
			width="10px"
			height="10px"
			viewBox="0 0 24 24"
			xmlns="http://www.w3.org/2000/svg"
			style="margin-top: 0;"
		>
			<path
				d="M11.178 19.569a.998.998 0 0 0 1.644 0l9-13A.999.999 0 0 0 21 5H3a1.002 1.002 0 0 0-.822 1.569l9 13z"
			/>
		</svg>
	</div>
</button>

<div class="card p-4 max-w-sm" data-popup="popupClick">
	<div class="grid grid-cols-1 gap-2">
		<div class="flex justify-between">
			<strong>Mode</strong>
			<LightSwitch />
		</div>
		<hr class="!border-t-2" />
		<a href="/" class="btn variant-filled" data-sveltekit-preload-data="hover">Home</a>
		<a href="/documentation" class="btn variant-filled" data-sveltekit-preload-data="hover"
			>Documentation</a
		>
		<a href="/login" class="btn variant-filled" data-sveltekit-preload-data="hover">Login</a>
	</div>
	<div class="arrow bg-surface-100-800-token"></div>
</div>
