<script>
	import FaAngellist from 'svelte-icons/fa/FaAngellist.svelte';
	import Button from './lib/Button.svelte';
	import FaAngelist from 'svelte-icons/fa/FaAngellist.svelte';
</script>

<Button let:x>
	<div style:width="20px" slot="leftContent"><FaAngellist></FaAngellist></div>
	Button {x}
</Button>

<style>
</style>
