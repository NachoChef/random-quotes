<script>
	import Quote from './Quote.svelte';
	import Button from './Button.svelte';
	import Footer from '$lib/Footer.svelte';
</script>

<div class="page-wrapper">
	<div class="button-wrapper">
		<Button />
	</div>
	<div class="quote-wrapper">
		<Quote />
	</div>
</div>

<Footer />

<style>
	:global(*) {
		font-family: 'Open Sans', sans-serif;
	}

	.page-wrapper {
		height: 100vh;
		display: flex;
		flex-direction: column;
	}

	.button-wrapper {
		justify-self: end;
	}

	.quote-wrapper {
		margin: auto;
		width: 50%;
	}
</style>
