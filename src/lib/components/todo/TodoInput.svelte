<script>
	import { deleteTodo, toggleComplete, editTodo } from '../../store/TodoStore';
	import { fade } from 'svelte/transition';

	export let todo;
	$: completeClass = todo.complete ? 'success' : 'info';
</script>

<!-- mobile -->
<div transition:fade class="flex flex-wrap items-center gap-4 sm:hidden">
	<div>
		<input
			disabled={todo.text.trim() === ''}
			type="checkbox"
			checked={todo.complete}
			class="checkbox-primary checkbox"
			id={`${todo.id}-checkbox`}
			on:change={() => toggleComplete(todo.id)}
		/>
	</div>
	<div class="grow">
		<input
			class="input-bordered input-ghost input w-full max-w-sm text-ellipsis"
			type="text"
			placeholder="Enter a Todo"
			value={todo.text}
			id={`${todo.id}-text`}
			on:input={(e) => editTodo(todo.id, e.target.value)}
		/>
	</div>
	<button
		class="btn-ghost btn-circle btn basis-full"
		type="button"
		on:click={() => deleteTodo(todo.id)}
	>
		<span class="sr-only">Delete Todo</span>
		<svg
			class="h-5 w-5"
			xmlns="http://www.w3.org/2000/svg"
			fill="none"
			stroke="currentColor"
			stroke-width="2"
			aria-hidden="true"
			viewBox="0 0 24 24"
			><path
				stroke-linecap="round"
				stroke-linejoin="round"
				d="m14.74 9-.346 9m-4.788 0L9.26 9m9.968-3.21c.342.052.682.107 1.022.166m-1.022-.165L18.16 19.673a2.25 2.25 0 0 1-2.244 2.077H8.084a2.25 2.25 0 0 1-2.244-2.077L4.772 5.79m14.456 0a48.108 48.108 0 0 0-3.478-.397m-12 .562c.34-.059.68-.114 1.022-.165m0 0a48.11 48.11 0 0 1 3.478-.397m7.5 0v-.916c0-1.18-.91-2.164-2.09-2.201a51.964 51.964 0 0 0-3.32 0c-1.18.037-2.09 1.022-2.09 2.201v.916m7.5 0a48.667 48.667 0 0 0-7.5 0"
			/></svg
		>
	</button>
	<div
		class="{`bg-${completeClass}`} badge basis-full text-base-100  transition-colors duration-150"
	>
		{todo.complete ? 'Complete' : 'In Progress'}
	</div>
</div>

<!-- and up -->
<div class="hidden items-center justify-between space-x-6 sm:flex" transition:fade>
	<div>
		<input
			disabled={todo.text.trim() === ''}
			type="checkbox"
			checked={todo.complete}
			class="checkbox-primary checkbox"
			id={`${todo.id}-checkbox`}
			on:change={() => toggleComplete(todo.id)}
		/>
	</div>
	<div class="w-full grow">
		<input
			class="input-bordered input-ghost input w-full max-w-md text-ellipsis"
			type="text"
			placeholder="Enter a Todo"
			value={todo.text}
			id={`${todo.id}-text`}
			on:input={(e) => editTodo(todo.id, e.target.value)}
		/>
	</div>

	<div
		class="{`bg-${completeClass}`} badge min-w-[100px] text-base-100 transition-colors duration-150"
	>
		{todo.complete ? 'Complete' : 'In Progress'}
	</div>
	<div class="grow" />
	<button class="btn-ghost btn-circle btn" type="button" on:click={() => deleteTodo(todo.id)}>
		<span class="sr-only">Delete Todo</span>
		<svg
			class="h-5 w-5"
			xmlns="http://www.w3.org/2000/svg"
			fill="none"
			stroke="currentColor"
			stroke-width="2"
			aria-hidden="true"
			viewBox="0 0 24 24"
			><path
				stroke-linecap="round"
				stroke-linejoin="round"
				d="m14.74 9-.346 9m-4.788 0L9.26 9m9.968-3.21c.342.052.682.107 1.022.166m-1.022-.165L18.16 19.673a2.25 2.25 0 0 1-2.244 2.077H8.084a2.25 2.25 0 0 1-2.244-2.077L4.772 5.79m14.456 0a48.108 48.108 0 0 0-3.478-.397m-12 .562c.34-.059.68-.114 1.022-.165m0 0a48.11 48.11 0 0 1 3.478-.397m7.5 0v-.916c0-1.18-.91-2.164-2.09-2.201a51.964 51.964 0 0 0-3.32 0c-1.18.037-2.09 1.022-2.09 2.201v.916m7.5 0a48.667 48.667 0 0 0-7.5 0"
			/></svg
		>
	</button>
</div>

<div class="divider" />
