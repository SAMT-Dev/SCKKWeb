<script lang="ts">
	import type { PageData } from './$types';

	let { data }: { data: PageData } = $props();
</script>

<svelte:head>
	<title>Névjegy - SCKK</title>
	<meta name="description" content="SCKK - Névjegy" />
	<meta content="See City Közlekedési Központ" property="og:title" />
	<meta content="/info" property="og:url" />
	<meta content="SCKK - Névjegy" property="og:description" />
</svelte:head>

<div
	class="3xl:w-[30dvw] border-taxi -z-10 mx-auto mt-4 flex w-[90dvw] flex-col gap-8 rounded-3xl border-2 bg-black/45 p-8 text-center xl:w-[50dvw] 2xl:w-[40dvw]"
>
	<div>
		<h2 class="font-montserrat text-taxi text-xl font-light xl:text-[40px]">
			Telephely: 1121, See City, El Corona 1
		</h2>
	</div>
	<div class="flex flex-col items-center justify-center gap-2 lg:flex-row lg:items-start lg:gap-8">
		<div class="flex flex-col items-center gap-2">
			<img src="/pics/diego_portrait.png" class="pointer-events-none w-64 select-none" alt="" />
			<div>
				<h2 class="font-nunito text-taxi text-xl font-bold">Vezérigazgató</h2>
				<h2 class="font-poppins font-light text-white">Diego M Perez</h2>
				<h2 class="font-poppins font-light text-white">+38-76-509-8320</h2>
			</div>
		</div>
		<div class="flex flex-col items-center gap-2">
			<img src="/pics/kevin_portrait.png" class="pointer-events-none w-64 select-none" alt="" />
			<div>
				<h2 class="font-nunito text-taxi text-xl font-bold">Vezérigazgató-helyettes</h2>
				<h2 class="font-poppins font-light text-white">Kevin Styles</h2>
				<h2 class="font-poppins font-light text-white">+38-76-615-2768</h2>
			</div>
		</div>
		<div class="flex flex-col items-center gap-2">
			<img src="/pics/hanrick_portrait.png" class="pointer-events-none w-64 select-none" alt="" />
			<div>
				<h2 class="font-nunito text-taxi text-xl font-bold">Gazdasági igazgató</h2>
				<h2 class="font-montserrat font-light text-white">John Hanrick</h2>
				<h2 class="font-montserrat font-light text-white">+38-76-972-6825</h2>
			</div>
		</div>
	</div>
</div>
