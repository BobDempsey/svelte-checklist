<script>
	import Navbar from '../lib/components/app/Navbar.svelte';
	import AddTodoSection from '../lib/components/todo/AddTodoSection.svelte';
	import TodoSection from '../lib/components/todo/TodoSection.svelte';
	import ProgressSection from '../lib/components/progress/ProgressSection.svelte';
	import AboutModal from '../lib/components/app/AboutModal.svelte';
	import GithubRepoBtn from '../lib/components/app/GithubRepoBtn.svelte';
</script>

<div class="flex min-h-screen flex-col bg-base-200">
	<Navbar />
	<main class="grow">
		<div class="selection:color-secondary selection:color-primary p-0 py-12 md:px-8 md:py-24">
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
	</main>

	<footer class="footer flex items-center justify-between p-2 text-xs sm:py-4 sm:px-6 sm:text-sm">
		<div class="flex items-center">
			&copy; {new Date().getFullYear()} |
			<a href="https://bobdempsey83.com" class="underline-offset-4 hover:underline">Bob Dempsey</a>
		</div>
		<div class="flex items-center sm:gap-4">
			<GithubRepoBtn />
			<AboutModal />
		</div>
	</footer>
</div>
