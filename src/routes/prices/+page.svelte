<script lang="ts">
	import type { PageData } from './$types';

	let { data }: { data: PageData } = $props();
</script>

<svelte:head>
	<title>Áraink - SCKK</title>
	<meta name="description" content="SCKK - Áraink" />
	<meta content="See City Közlekedési Központ" property="og:title" />
	<meta content="/prices" property="og:url" />
	<meta content="SCKK - Áraink" property="og:description" />
</svelte:head>

<div
	class="border-taxi font-montserrat absolute top-1/2 left-1/2 -z-10 -translate-x-1/2 -translate-y-1/2 rounded-3xl border-2 bg-black/45 p-8 text-center text-white lg:w-[30dvw] md:w-[50dvw] w-[90dvw]"
>
	<h1 class="text-taxi font-nunito text-5xl font-bold xl:text-3xl">Áraink</h1>
	<div class="flex gap-2">
			<div>
				<h2 class="font-bold">15:00 - 22:00</h2>
				<h2 class="font-light">2500 $/km, 350 $/perc</h2>
			</div>
			<div>
				<h2 class="font-bold">Idősávokon kívül</h2>
				<h2 class="font-light">4000 $/km, 400 $/perc</h2>
			</div>
		</div>
		<h1 class="text-gray-400">Utoljára módosítva: 2025.07.03.</h1>
</div>
