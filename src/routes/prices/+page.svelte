<script lang="ts">
	import type { PageData } from './$types';

	let { data }: { data: PageData } = $props();
</script>

<svelte:head>
	<title>Áraink - SCKK</title>
</svelte:head>

<div
	class="border-taxi font-montserrat absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 rounded-3xl border-2 bg-black/45 p-8 text-center text-white"
>
	<h1 class="text-taxi font-nunito text-5xl font-bold xl:text-3xl">Áraink</h1>
	<div class="flex gap-8">
		<div class="flex flex-col items-center gap-2">
			<h2 class="font-poppins text-3xl font-light text-cyan-400">Hétköznap</h2>
			<div>
				<h2 class="font-bold">15:00 - 18:30</h2>
				<h2 class="font-light">2600 $/km, 350 $/perc</h2>
			</div>
			<div>
				<h2 class="font-bold">18:30 - 22:00</h2>

				<h2 class="font-light">2500 $/km, 350 $/perc</h2>
			</div>
			<div>
				<h2 class="font-bold">Idősávokon kívül</h2>
				<h2 class="font-light">3800 $/km, 400 $/perc</h2>
			</div>
		</div>
		<div class="flex flex-col items-center gap-2">
			<h2 class="font-poppins text-3xl font-light text-cyan-400">Hétvégén</h2>
			<div>
				<h2 class="font-bold">15:00 - 22:00</h2>
				<h2 class="font-light">2600 $/km, 250 $/perc</h2>
			</div>
			<div>
				<h2 class="font-bold">Idősávokon kívül</h2>
				<h2 class="font-light">3500 $/km, 300 $/perc</h2>
			</div>
		</div>
	</div>
</div>
