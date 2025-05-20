<script lang="ts">
	import type { PageData } from './$types';

	let { data }: { data: PageData } = $props();
</script>

<div
	class="3xl:w-[30dvw] border-taxi absolute top-1/2 left-1/2 flex w-[90dvw] -translate-x-1/2 -translate-y-1/2 flex-col gap-8 rounded-3xl border-2 bg-black/45 p-8 text-center xl:w-[50dvw] 2xl:w-[40dvw]"
>
	<div>
		<h2 class="font-montserrat text-taxi text-xl font-light xl:text-[40px]">
			Telephely: 1121, See City, El Corona 1
		</h2>
	</div>
	<div class="flex items-center justify-center gap-8">
		<div class="flex flex-col items-center gap-2">
			<img src="/pics/diego_m_perez.jpg" class="w-64" alt="" />
			<div>
				<h2 class="font-nunito text-taxi text-xl font-bold">Vezérigazgató</h2>
				<h2 class="font-poppins font-light text-white">Diego M Perez</h2>
				<h2 class="font-poppins font-light text-white">+38-76-509-8320</h2>
			</div>
		</div>
		<div class="flex flex-col items-center gap-2">
			<img src="/pics/kevin_styles.jpg" class="w-64" alt="" />
			<div>
				<h2 class="font-nunito text-taxi text-xl font-bold">Vezérigazgató-helyettes</h2>
				<h2 class="font-poppins font-light text-white">Kevin Styles</h2>
				<h2 class="font-poppins font-light text-white">+38-76-615-2768</h2>
			</div>
		</div>
		<div class="flex flex-col items-center gap-2">
			<img src="/pics/john_hanrick.png" class="w-64" alt="" />
			<div>
				<h2 class="font-nunito text-taxi text-xl font-bold">Gazdasági igazgató</h2>
				<h2 class="font-montserrat font-light text-white">John Hanrick</h2>
				<h2 class="font-montserrat font-light text-white">-</h2>
			</div>
		</div>
	</div>
</div>
