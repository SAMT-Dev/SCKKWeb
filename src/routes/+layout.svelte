<script lang="ts">
	import { page } from '$app/state';
	import '../app.css';

	let { children } = $props();

	let nav: HTMLDivElement = $state()!;
	const tognav = () => {
		if (nav.classList.contains('hidden')) {
			nav.classList.remove('hidden');
			nav.classList.add('flex');
		} else {
			nav.classList.remove('flex');
			nav.classList.add('hidden');
		}
	};
</script>

<svelte:head>
	<title>See City Közlekedési Központ</title>
	<meta name="description" content="A See City Közlekedési Központ weboldala." />
	<meta content="SCKK Weboldal" property="og:title" />
	<meta content="/" property="og:url" />
	<meta content="A See City Közlekedési Központ weboldala." property="og:description" />
	<meta content="/favicon.png" property="og:image" />
	<meta content="#fece01" data-react-helmet="true" name="theme-color" />
</svelte:head>

<div
	class="absolute top-1/2 left-1/2 -z-50 h-[100%] w-[100%] -translate-x-1/2 -translate-y-1/2 overflow-hidden bg-black bg-[url(/backgrounds/bg-2.png)] bg-cover bg-no-repeat"
></div>

<header
	class="4xl:px-[20dvw] z-50 grid grid-cols-2 items-center justify-between gap-4 bg-black/70 px-2 py-2 md:px-8 lg:flex lg:px-[8dvw]"
>
	<a href="/">
		<img
			src="/base.png"
			alt="sckk_poster"
			class="pointer-events-none hidden w-[300px] select-none sm:block lg:w-[450px]"
		/>
		<div class="flex items-center gap-2 sm:hidden">
			<img src="/favicon.png" alt="" class="pointer-events-none h-[30px]" />
			<h1 class="font-nunito text-xl font-bold text-white">SCKK</h1>
		</div>
	</a>
	<button
		aria-label="mv-menu"
		class="hover:text-taxi flex cursor-pointer justify-self-end text-3xl font-semibold text-white transition-all duration-200 lg:hidden"
		onclick={tognav}
	>
		<span class="icon-[material-symbols--menu]"></span>
	</button>
	<div
		bind:this={nav}
		class="font-montserrat col-span-2 hidden flex-col items-center justify-center gap-4 text-center font-bold text-white uppercase lg:flex lg:flex-row lg:gap-8 lg:text-xl xl:gap-12"
	>
		<a
			class="hover:text-taxi transition-all duration-200"
			class:text-taxi={page.url.pathname === '/'}
			href="/">Főoldal</a
		>
		<a
			class="hover:text-taxi transition-all duration-200"
			class:text-taxi={page.url.pathname === '/info'}
			href="/info">Névjegy</a
		>
		<a
			class="hover:text-taxi transition-all duration-200"
			class:text-taxi={page.url.pathname === '/prices'}
			href="/prices">Áraink</a
		>
		<a class="hover:text-taxi transition-all duration-200" href="/jelentkezes" target="_blank"
			>Jelentkezés</a
		>
		<a class="text-rose-500 transition-all duration-200 hover:text-red-400" href="https://samt.hu"
			>SAMT</a
		>
	</div>
</header>

{@render children()}

<h1
	class="font-nunito pointer-events-none fixed bottom-2 left-1/2 -translate-x-1/2 cursor-move text-center font-medium text-white select-none text-shadow-black text-shadow-lg"
>
	Fiktív játékbeli vállalkozás | © {new Date().getFullYear()} See City Közlekedési Központ
</h1>
