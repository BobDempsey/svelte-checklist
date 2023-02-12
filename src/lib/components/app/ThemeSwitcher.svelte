<script>
	// https://github.com/spences10/sveltekit-theme-switch-example
	import { onMount } from 'svelte';
	import { themeChange } from 'theme-change';

	function capitalizeFirstLetter(str) {
		if (!str) return;
		return str.charAt(0).toUpperCase() + str.slice(1);
	}

	onMount(() => {
		themeChange(false);
	});

	const themes = [
		'light',
		'dark',
		'acid',
		'aqua',
		'autumn',
		'black',
		'bumblebee',
		'business',
		'cmyk',
		'coffee',
		'corporate',
		'cupcake',
		'cyberpunk',
		'dracula',
		'emerald',
		'fantasy',
		'forest',
		'garden',
		'halloween',
		'lemonade',
		'lofi',
		'luxury',
		'night',
		'pastel',
		'retro',
		'synthwave',
		'valentine',
		'winter',
		'wireframe'
	];
</script>

<select data-choose-theme class="select-bordered select-primary select w-full max-w-3xl text-lg">
	<option disabled="disabled" selected="selected">Set Theme 🎨</option>
	{#each themes as theme}
		<option value={theme}>{capitalizeFirstLetter(theme)}</option>
	{/each}
</select>
