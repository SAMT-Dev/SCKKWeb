<script lang="ts">
	import type { PageData } from './$types';

	let { data }: { data: PageData } = $props();
</script>

<svelte:head>
	<title>VIP Csomagjaink - SCKK</title>
	<meta name="description" content="SCKK - VIP Csomagjaink" />
	<meta content="See City Közlekedési Központ" property="og:title" />
	<meta content="/info" property="og:url" />
	<meta content="SCKK - VIP Csomagjaink" property="og:description" />
</svelte:head>

<div
	class="3xl:w-[30dvw] border-taxi -z-10 mx-auto mt-4 flex w-[90dvw] flex-col gap-8 rounded-3xl border-2 bg-black/45 p-8 text-center xl:w-[50dvw] 2xl:w-[40dvw]"
>
	<div class="text-white">
		<h2 class="font-montserrat text-taxi text-3xl font-light xl:text-[40px]">VIP Csomagjaink</h2>
		<h2>
			További részletekért: <a
				href="/vip-info"
				target="_blank"
				class="text-taxi font-montserrat font-bold">KATT</a
			>
		</h2>
		<a class="font-nunito text-taxi mt-2 text-xl font-bold uppercase" href="/vip-minta"
			>Igényelj még ma!</a
		>
	</div>
	<div class="flex flex-col items-center justify-center gap-2 lg:items-center lg:gap-8">
		<div class="flex flex-col items-center gap-2">
			<h2 class="font-nunito text-3xl font-bold text-amber-900">Bronz</h2>
			<div>
				<h2 class="font-poppins text-xl font-light text-white">
					Tarifa: <span class="font-bold text-green-500">2000$/km</span>,
					<span class="font-bold text-green-500">200$/perc</span>
				</h2>
				<h2 class="font-poppins text-xl font-light text-white">
					Bérlési kedvezmény: <span class="font-bold text-green-500">20%</span>
				</h2>
			</div>
			<h2 class="font-poppins text-2xl font-bold text-green-500">50.000$/hét</h2>
		</div>
		<div class="flex flex-col items-center gap-2">
			<h2 class="font-nunito text-3xl font-bold text-gray-400">Ezüst</h2>
			<div>
				<h2 class="font-poppins text-xl font-light text-white">
					Tarifa: <span class="font-bold text-green-500">1500$/km</span>,
					<span class="font-bold text-green-500">150$/perc</span>
				</h2>
				<h2 class="font-poppins text-xl font-light text-white">
					Bérlési kedvezmény: <span class="font-bold text-green-500">30%</span>
				</h2>
			</div>
			<h2 class="font-poppins text-2xl font-bold text-green-500">80.000$/hét</h2>
		</div>
		<div class="flex flex-col items-center gap-2">
			<h2 class="font-nunito text-3xl font-bold text-yellow-600">Arany</h2>
			<div>
				<h2 class="font-poppins text-xl font-light text-white">
					Tarifa: <span class="font-bold text-green-500">1000$/km</span>,
					<span class="font-bold text-green-500">100$/perc</span>
				</h2>
				<h2 class="font-poppins text-xl font-light text-white">
					Bérlési kedvezmény: <span class="font-bold text-green-500">40%</span>
				</h2>
			</div>
			<h2 class="font-poppins text-2xl font-bold text-green-500">100.000$/hét</h2>
		</div>
		<div class="flex flex-col items-center gap-2">
			<h2 class="font-nunito text-3xl font-bold text-blue-600">Platina</h2>
			<div>
				<h2 class="font-poppins text-xl font-light text-white">
					Tarifa: <span class="font-bold text-green-500">0$/km</span>,
					<span class="font-bold text-green-500">0$/perc</span>
				</h2>
				<h2 class="font-poppins text-xl font-light text-white">
					Bérlési kedvezmény: <span class="font-bold text-green-500">50%</span>
				</h2>
			</div>
			<h2 class="font-poppins text-2xl font-bold text-green-500">200.000$/hét</h2>
		</div>
	</div>
</div>
