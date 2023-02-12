<script>
	import ThemeSwitcher from './ThemeSwitcher.svelte';
</script>

<div class="navbar bg-base-200">
	<!-- brand -->
	<div class="flex-1">
		<a class="btn-ghost btn gap-2 text-xl normal-case" href="https://bobdempsey83.com">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				fill="none"
				stroke="currentColor"
				stroke-width="2"
				aria-hidden="true"
				class="h-5 w-5"
				viewBox="0 0 24 24"
				><path
					stroke-linecap="round"
					stroke-linejoin="round"
					d="M19.5 12h-15m0 0 6.75 6.75M4.5 12l6.75-6.75"
				/></svg
			>
			<span class="sm:hidden">BD</span>
			<span class="hidden sm:block">Bob Dempsey</span>
		</a>
	</div>
	<!-- theme switcher -->
	<div class="mr-4 flex-none">
		<ThemeSwitcher />
	</div>
</div>
