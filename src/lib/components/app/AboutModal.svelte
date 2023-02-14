<!-- The button(label) to open modal -->
<label for="my-modal-4" class="btn-ghost btn-circle btn absolute bottom-5 right-5">
	<svg
		class="h-6 w-6"
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
			d="M11.25 11.25l.041-.02a.75.75 0 011.063.852l-.708 2.836a.75.75 0 001.063.853l.041-.021M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-9-3.75h.008v.008H12V8.25z"
		/>
	</svg>
</label>

<!-- Put this part before </body> tag -->
<input type="checkbox" id="my-modal-4" class="modal-toggle" />
<label for="my-modal-4" class="modal cursor-pointer">
	<label class="modal-box relative" for="">
		<h3 class="text-lg font-bold">About This App</h3>
		<p class="py-4">
			A to-do app using SvelteKit, Tailwind CSS, Daisy UI, and local storage persistence. CI/CD and
			hosting on Vercel.
		</p>
	</label>
</label>
