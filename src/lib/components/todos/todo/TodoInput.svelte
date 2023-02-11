<script>
	import { deleteTodo, toggleComplete, editTodo } from '../../../store/TodoStore';

	export let todo;
</script>

<div class="flex items-center justify-between rounded-md border-2 border-base-300 px-5 py-4">
	<div class="flex w-full max-w-lg items-center justify-start">
		<div class="form-control">
			<label class="label cursor-pointer" for={`${todo.id}-checkbox`}>
				<span class="label-text sr-only">Complete Todo</span>
				<input
					type="checkbox"
					checked={todo.complete}
					class="checkbox-primary checkbox"
					id={`${todo.id}-checkbox`}
					on:change={() => toggleComplete(todo.id)}
				/>
			</label>
		</div>

		<div class="form-control w-full max-w-xs">
			<label class="label" for={`${todo.id}-text`}>
				<span class="label-text sr-only">Edit Todo</span>
				<span class="label-text-alt">Alt label</span>
			</label>
			<input
				class="input-bordered input ml-5 w-full max-w-xs text-ellipsis"
				type="text"
				placeholder="Enter a Todo"
				value={todo.text}
				id={`${todo.id}-text`}
				on:input={(e) => editTodo(todo.id, e.target.value)}
			/>

			{#if todo.complete}
				<div class="badge-success badge">Complete</div>
			{:else}
				<div class="badge-info badge">In Progress</div>
			{/if}

			<label class="label" for={`${todo.id}-text`}>
				<span>{todo.complete ? 'Complete' : 'In Progress'}</span>

				<span class="label-text-alt">Alt label</span>
				<span class="label-text-alt">Alt label</span>
			</label>
		</div>
		<div>
			<button class="btn-circle btn" type="button" on:click={() => deleteTodo(todo.id)}>
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
	</div>
</div>
