<script lang="ts">
	import { page } from '$app/state';
	import '../app.css';

	let { children } = $props();
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
	class="4xl:px-[20dvw] flex items-center justify-between gap-4 bg-black/70 px-8 py-2 lg:px-[8dvw]"
>
	<a href="/">
		<img
			src="/base.png"
			alt="sckk_poster"
			class="pointer-events-none w-[300px] select-none lg:w-[450px]"
		/>
	</a>
	<div
		class="font-montserrat flex items-center justify-center gap-4 text-center font-bold text-white uppercase lg:gap-8 lg:text-xl xl:gap-12"
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
	class="font-nunito pointer-events-none absolute right-2 bottom-2 cursor-move font-medium text-white select-none"
>
	2025 - sckk.hu
</h1>
