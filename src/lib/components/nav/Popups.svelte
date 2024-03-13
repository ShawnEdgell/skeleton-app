<script lang="ts">
	import { popup, LightSwitch } from '@skeletonlabs/skeleton';
</script>

{#each ['Explore', 'Header 1', 'Header 2'] as label, i}
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
			<div class="popup-menu flex flex-col space-y-4">
				<div class="flex justify-between">
					<span class="font-bold">Mode</span>
					<LightSwitch />
				</div>
				<hr class="!border-t-2" />
				<a
					href="/"
					class="btn bg-primary-hover-token variant-filled-900"
					data-sveltekit-preload-data="hover">Homepage</a
				>
				<a
					href="/docs"
					class="btn bg-primary-hover-token variant-filled-900"
					data-sveltekit-preload-data="hover">Documentation</a
				>
				<a
					href="/blog"
					class="btn bg-primary-hover-token variant-filled-900"
					data-sveltekit-preload-data="hover">Blog</a
				>
				<hr class="!border-t-2" />
				<a
					href="/skaterxl"
					class="btn bg-primary-hover-token variant-filled-900"
					data-sveltekit-preload-data="hover">Skater XL</a
				>
				<a
					href="/session"
					class="btn bg-primary-hover-token variant-filled-900"
					data-sveltekit-preload-data="hover">Session</a
				>
				<a
					href="/skate"
					class="btn bg-primary-hover-token variant-filled-900"
					data-sveltekit-preload-data="hover">Skate</a
				>
			</div>
		{:else if label === 'Header 1'}
			<button type="button" class="btn variant-filled">Button</button>
		{:else if label === 'Header 2'}
			<button type="button" class="btn variant-filled">Button</button>
		{/if}
	</div>
{/each}
