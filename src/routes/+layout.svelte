<script lang="ts">
	import { page } from '$app/state';
	import '../app.css';

	let { children } = $props();

	let navcucc: HTMLElement = $state()!;
	const tognav = () => {
		if (navcucc.classList.contains('hidden')) {
			navcucc.classList.remove('hidden');
			navcucc.classList.add('flex');
		} else {
			navcucc.classList.remove('flex');
			navcucc.classList.add('hidden');
		}
	};
</script>

<svelte:head>
	<title>See City Közlekedési Központ</title>
	<meta name="description" content="SCKK - Veled, minden úton!" />
	<meta content="See City Közlekedési Központ" property="og:title" />
	<meta content="/" property="og:url" />
	<meta content="SCKK - Veled, minden úton!" property="og:description" />
	<meta content="/favicon.png" property="og:image" />
	<meta content="#fece01" data-react-helmet="true" name="theme-color" />
</svelte:head>

<!-- <div
	class="absolute top-1/2 left-1/2 -z-50 h-[100%] w-[100%] -translate-x-1/2 -translate-y-1/2 overflow-hidden bg-black bg-[url(/backgrounds/bg-2.png)] bg-cover bg-no-repeat"
></div> -->

<a
	href="https://seeweb.hu"
	target="_blank"
	class="absolute top-1/2 left-6 -z-40 hidden -translate-y-1/2 lg:block"
>
	<img src="/seeweb.png" alt="" width="200px" class="rounded-xl border-4 border-white" />
</a>

<header
	class="4xl:px-[20dvw] fixed top-0 z-50 grid w-full grid-cols-2 items-center justify-between gap-4 bg-black/70 px-2 py-2 md:px-8 xl:flex 2xl:px-[8dvw]"
>
	<a href="/">
		<img
			src="/base.png"
			alt="sckk_poster"
			class="pointer-events-none hidden w-[300px] select-none sm:block lg:w-[450px]"
		/>
		<div class="flex items-center gap-2 sm:hidden">
			<img src="/favicon.png" alt="" class="pointer-events-none" width="30px" height="30px" />
			<h1 class="font-nunito text-xl font-bold text-white">SCKK</h1>
		</div>
	</a>
	<button
		aria-label="mv-menu"
		class="hover:text-taxi flex cursor-pointer justify-self-end text-3xl font-semibold text-white transition-all duration-200 xl:hidden"
		onclick={tognav}
	>
		<span class="icon-[material-symbols--menu]"></span>
	</button>
	<nav
		bind:this={navcucc}
		class="font-montserrat col-span-2 hidden flex-col items-center justify-center gap-4 text-center font-bold text-white uppercase lg:gap-8 lg:text-xl xl:flex xl:flex-row 2xl:gap-12"
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
		<a
			class="hover:text-taxi transition-all duration-200"
			class:text-taxi={page.url.pathname === '/vip'}
			href="/vip">VIP</a
		>
		<a class="hover:text-taxi transition-all duration-200" href="/tgf" target="_blank"
			>Jelentkezés</a
		>
		<a class="hover:text-taxi transition-all duration-200" href="/pk" target="_blank">Panaszkönyv</a
		>
		<a class="text-rose-500 transition-all duration-200 hover:text-red-400" href="https://samt.hu"
			>Belépés</a
		>
	</nav>
</header>
<div class="mt-20 pb-16">
	{@render children()}
</div>
<footer
	class="font-nunito fixed bottom-0 mt-2 w-full bg-emerald-700 py-2 text-center font-medium text-white"
>
	<h1>Fiktív játékbeli vállalkozás</h1>
	<h1>
		© 2016-{new Date().getFullYear()} See City Közlekedési Központ,
	</h1>
	<h2>
		Támogatója a <a href="https://seeweb.hu" target="_blank" class="font-bold text-[#4dd097]"
			>SeeWEB</a
		>.
	</h2>
</footer>
