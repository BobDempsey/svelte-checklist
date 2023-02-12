<script>
	import AddTodoSection from '../lib/components/todo/AddTodoSection.svelte';
	import TodoSection from '../lib/components/todo/TodoSection.svelte';
	import ProgressSection from '../lib/components/progress/ProgressSection.svelte';
</script>

<div
	class="selection:color-secondary selection:color-primary min-h-screen bg-base-200 p-0  py-12 md:px-8 md:py-24"
>
	<div
		class="mx-6 max-w-5xl rounded-2xl bg-gradient-to-r from-primary via-info to-secondary p-1 md:mx-auto"
	>
		<div class="card bg-base-100">
			<div class="card-body space-y-8">
				<AddTodoSection />
				<TodoSection />
				<ProgressSection />
			</div>
		</div>
	</div>
</div>
