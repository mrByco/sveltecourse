<script>
	import FaAngellist from 'svelte-icons/fa/FaAngellist.svelte';
	import Button from './lib/Button.svelte';
	import FaAngelist from 'svelte-icons/fa/FaAngellist.svelte';

	function click() {
		alert('clicked');
	}
</script>

<Button
	disabled
	on:click|once={(event) => alert(JSON.stringify(event))}
	on:mousedown={() => alert('asd')}
	let:isLeftHovered
>
	<div style:width="20px" slot="leftContent"><FaAngellist></FaAngellist></div>
	Button {isLeftHovered}
</Button>

<style>
</style>
