<script lang="ts">
	export let quoteText =
		'Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur deleniti provident, nontempore dolores asperiores optio, iusto deserunt aut magnam odio consectetur voluptatum animivoluptatem hic modi aliquam laudantium minima!';
	export let quoteSource = 'Caesar';
	export let topic = 'Rome';
</script>

<div class="quote-wrapper">
	<div class="quote-text pad">
		{quoteText}
	</div>
	<div class="source pad">
		{quoteSource}
	</div>
	<div class="topic pad">
		{topic}
	</div>
</div>

<style>
	.pad {
		padding-left: 50px;
	}
	.quote-text {
		border-left: 4px solid rgb(216, 216, 3);
		font-size: large;
	}

	.source {
		padding-top: 75px;
		color: #444;
	}
	.topic {
		font-size: x-small;
		color: #444;
	}
</style>
