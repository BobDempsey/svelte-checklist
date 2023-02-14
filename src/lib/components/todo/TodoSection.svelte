<script>
	import TodoInput from './TodoInput.svelte';
	import { todos } from '../../store/TodoStore';
	import { fade } from 'svelte/transition';
</script>

{#if $todos.length}
	<section class="space-y-4">
		{#each $todos as todo (todo.id)}
			<TodoInput {todo} />
		{/each}
	</section>
{:else}
	<p class="text-lg font-semibold" transition:fade>Add a new todo to get started! 🤓</p>
{/if}
