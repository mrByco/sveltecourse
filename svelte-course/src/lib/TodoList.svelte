<script>
	import Button from './Button.svelte';
	import { v4 as uuid } from 'uuid';

	export let todos = [];

	let inputText = 'default';

	function handleAddTodo() {
		if (!inputText) return;
		todos.push({
			id: uuid(),
			title: inputText,
			completed: false
		});
		todos = todos;
		inputText = '';
	}
</script>

<div class="todo-list-wrapper">
	<ul>
		{#each todos as { title, id }, index (id)}
			{@const number = index + 1}
			<li>{number}. {title}</li>
		{/each}
	</ul>
	<form class="add-todo-form" on:submit|preventDefault={handleAddTodo}>
		<input bind:value={inputText} />
		<Button disabled={!inputText} type="submit">Add</Button>
	</form>
</div>
