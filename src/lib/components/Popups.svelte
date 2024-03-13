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

{#each ['Explore', 'Header 1', 'Header 2', 'Header 3'] as label, i}
	<!-- Trigger -->
	<button
		class="btn bg-primary-hover-token variant-filled-900"
		use:popup={{ event: 'click', target: 'loopExample-' + i, placement: 'top' }}
	>
		<div class="flex items-center gap-1">
			{label}
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
	<!-- Popup -->
	<div class="card p-4 max-w-sm" data-popup="loopExample-{i}">
		{#if label === 'Explore'}
			<div class="popup-menu">
				<div class="flex justify-between">
					<span class="font-bold">Mode</span>
					<LightSwitch />
				</div>
				<hr class="!border-t-2" />
				<a href="/" class="btn variant-filled">Homepage</a>
				<a href="/docs" class="btn variant-filled">Documentation</a>
				<a href="/blog" class="btn variant-filled">Blog</a>
				<hr class="!border-t-2" />
				<a href="/skaterxl" class="btn variant-filled">Skater XL</a>
				<a href="/session" class="btn variant-filled">Session</a>
				<a href="/skate" class="btn variant-filled">Skate</a>
			</div>
		{:else if label === 'Header 1'}
			<button type="button" class="btn variant-filled">Button</button>
		{:else if label === 'Header 2'}
			<button type="button" class="btn variant-filled">Button</button>
		{:else if label === 'Header 3'}
			<button type="button" class="btn variant-filled">Button</button>
		{/if}
	</div>
{/each}
