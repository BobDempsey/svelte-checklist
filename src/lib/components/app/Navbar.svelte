<div class="navbar bg-base-200">
	<!-- brand -->
	<div class="flex-1">
		<a class="btn-ghost btn gap-2 text-xl normal-case" href="https://bobdempsey83.com">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				fill="none"
				stroke="currentColor"
				stroke-width="2"
				aria-hidden="true"
				class="h-5 w-5"
				viewBox="0 0 24 24"
				><path
					stroke-linecap="round"
					stroke-linejoin="round"
					d="M19.5 12h-15m0 0 6.75 6.75M4.5 12l6.75-6.75"
				/></svg
			>
			<span>Bob Dempsey</span>
		</a>
	</div>
	<!-- theme switcher -->
	<div class="flex-none">
		<ul class="menu menu-horizontal z-50 mr-4 px-1">
			<li>
				<button> Set Theme 🎨 </button>
				<ul class="max-h-96 w-full overflow-y-scroll bg-base-100 p-2">
					<form method="POST">
						<li>
							<button formaction="/?/setTheme&theme=dark">Dark</button>
						</li>
						<li>
							<button formaction="/?/setTheme&theme=light">Light</button>
						</li>
					</form>
				</ul>
			</li>
		</ul>
	</div>
</div>
