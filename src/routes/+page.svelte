<script>
	import Quote from './Quote.svelte';
	import Button from './Button.svelte';
	import Footer from '$lib/Footer.svelte';
	import { onMount } from 'svelte';

	let quoteText =
		'Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur deleniti provident, nontempore dolores asperiores optio, iusto deserunt aut magnam odio consectetur voluptatum animivoluptatem hic modi aliquam laudantium minima!';
	let quoteAuthor = 'Caesar';
	let quoteGenre = 'Rome';

	onMount(async function () {
		newQuote();
	});

	async function newQuote() {
		const res = await fetch('https://quote-garden.herokuapp.com/api/v3/quotes');
		const data = await res.json();
		const quoteData = data['data'];
		quoteText = quoteData['quoteText'];
		quoteAuthor = quoteData['quoteAuthor'];
		quoteGenre = quoteData['quoteGenre'];
	}
</script>

<div class="page-wrapper">
	<div class="button-wrapper">
		<Button on:click={newQuote} />
	</div>
	<div class="quote-wrapper">
		<Quote {quoteText} {quoteAuthor} {quoteGenre} />
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
