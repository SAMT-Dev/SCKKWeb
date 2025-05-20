<script lang="ts">
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
	class="absolute top-1/2 left-1/2 -z-50 h-[100%] w-[100%] -translate-x-1/2 -translate-y-1/2 overflow-hidden bg-black bg-[url(/backgrounds/bg-1.png)] bg-cover bg-no-repeat"
></div>

<header
	class="4xl:px-[20dvw] flex items-center justify-between gap-4 bg-black/70 px-8 py-2 lg:px-[8dvw]"
>
	<img src="/base.png" alt="sckk_poster" class="pointer-events-none w-[300px] lg:w-[450px]" />
	<div
		class="font-montserrat flex items-center justify-center gap-4 text-center font-bold text-white uppercase lg:gap-8 lg:text-xl xl:gap-12"
	>
		<a href="/">Főoldal</a>
		<a href="/">Névjegy</a>
		<a href="/">Áraink</a>
		<a href="/">Jelentkezés</a>
		<a href="https://samt.hu">SAMT UCP</a>
	</div>
</header>

{@render children()}
