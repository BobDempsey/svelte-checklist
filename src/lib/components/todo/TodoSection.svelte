<script>
	import TodoInput from './TodoInput.svelte';
	import { todos } from '../../store/TodoStore';
</script>

{#if $todos.length}
	<section class="space-y-4">
		{#each $todos as todo (todo.id)}
			<TodoInput {todo} />
		{/each}
	</section>
{/if}
