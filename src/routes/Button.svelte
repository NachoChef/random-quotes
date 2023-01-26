<script>
	import Autorenew from 'svelte-material-icons/Autorenew.svelte';
</script>

<button on:click>
	random
	<span class="icon">
		<Autorenew />
	</span>
</button>

<style>
	button {
		float: right;
		height: 30px;
		background: none;
		border: 0;
		font-size: smaller;
		color: #444;
		cursor: pointer;
		display: inline-block;
	}

	.icon {
		padding-left: 5px;
	}
</style>
