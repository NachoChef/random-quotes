<script lang="ts">
	export let quoteText: string;
	export let quoteAuthor: string;
	export let quoteGenre: string;
</script>

<div class="quote-wrapper">
	<div class="quote-text pad">
		{quoteText}
	</div>
	<div class="source pad">
		{quoteAuthor}
	</div>
	<div class="topic pad">
		{quoteGenre}
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
