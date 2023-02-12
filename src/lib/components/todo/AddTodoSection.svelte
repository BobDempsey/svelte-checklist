<script>
	import { addTodo } from '../../store/TodoStore';
</script>

<section class="relative flex items-center justify-between">
	<h3
		class="-mt-4 -ml-2 max-w-[200px] bg-gradient-to-r from-primary to-secondary bg-clip-text text-4xl font-bold text-transparent sm:ml-1 sm:mt-0 sm:max-w-full"
	>
		Svelte Tailwind Todo List
	</h3>

	<button
		class="btn-primary btn absolute -top-5 -right-5 sm:gap-2"
		type="button"
		on:click={addTodo}
	>
		<span class="hidden sm:block">Add Task</span>
		<svg
			class="h-6 w-6 sm:h-5 sm:w-5"
			fill="none"
			stroke="currentColor"
			stroke-width="2"
			viewBox="0 0 24 24"
			xmlns="http://www.w3.org/2000/svg"
			aria-hidden="true"
		>
			<path
				stroke-linecap="round"
				stroke-linejoin="round"
				d="M12 9v6m3-3H9m12 0a9 9 0 11-18 0 9 9 0 0118 0z"
			/>
		</svg>
	</button>
</section>
