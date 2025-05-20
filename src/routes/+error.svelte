<script lang="ts">
	import { page } from '$app/state';
	import { onMount } from 'svelte';
	onMount(async () => {
		if (page.status === 404) {
			window.location.href = `https://samt.hu/s${page.url.pathname}`;
		}
	});
</script>

<main class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 text-center">
	{#if page.status === 404}
		<h1 class="font-poppins text-3xl font-bold text-white">Át leszel irányítva! 😍</h1>
	{/if}
</main>
