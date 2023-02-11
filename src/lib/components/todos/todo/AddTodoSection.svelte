<script>
	import { addTodo } from '../../../store/TodoStore';
</script>

<section class="flex justify-between">
	<h3 class="text-xl font-bold ">Checklist</h3>

	<button class="btn gap-2" type="button" on:click={addTodo}>
		Add Task
		<svg
			class="h-5 w-5"
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
