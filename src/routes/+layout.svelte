<script>
	import "../styles.scss";
	import AOS from "aos";
	import { onMount } from "svelte";
	import "aos/dist/aos.css";
	onMount(() => {
		AOS.init();
		setTimeout(() => {
			isLoading = false;
		}, 1000);
	});

	let isLoading = true;
</script>

<div class="app">
	{#if isLoading}
		<div class="loading-container">
			<svg class="logo">
				<svg
					class="u-inline-block u-valign-middle u-fit-w"
					enable-background="new 0 0 366.9 127.6"
					version="1.1"
					viewBox="0 0 373.00001 128"
					xml:space="preserve"
					xmlns="http://www.w3.org/2000/svg"
				>
					<polygon
						transform="translate(6.1 .4)"
						points="31.6 44.6 25.3 51 38 63.8 25.3 76.6 31.6 82.9 47.4 67 47.4 60.6"
					/>
					<polygon
						transform="translate(6.1 .4)"
						points="0 63.8 63.2 0 75.9 0 12.6 63.8 75.9 127.6 63.2 127.6"
					/>
					<path
						d="m221.2 0.4h-6.3l-38 38.3-38-38.3h-6.3l-60.1 60.6v6.4l60.1 60.6h6.3l38-38.3 38 38.3h6.3l60.1-60.6v-6.4zm-85.5 118-53.7-54.2 53.8-54.2 34.9 35.1-15.9 15.9v6.4l15.8 16zm41.2-66.9 12.7 12.7-12.7 12.8-12.6-12.8zm41.1 66.9-34.8-35 15.8-16v-6.4l-15.9-15.9 34.9-35.1 53.8 54.2z"
					/>
					<path
						d="m284.4 128 60.1-60.6v-6.4l-60.1-60.6h-12.7l63.4 63.8-63.3 63.8z"
					/>
					<path
						d="m373 128-63.3-63.8 63.3-63.8h-12.6l-60.1 60.6v6.4l60.1 60.6z"
					/>
					<rect width="9.5" height="127.6" />
				</svg>
			</svg>
		</div>
	{:else}
		<main>
			<slot />
		</main>
	{/if}
</div>

<style>
	.loading-container {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
	}

	.logo {
		fill: #215732;
		width: 100px; /* Ubah ukuran logo sesuai kebutuhan */
		height: 100px;
	}
</style>
