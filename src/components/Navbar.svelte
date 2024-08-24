<div class="navbar bg-transparent fixed">
	<div class="navbar-start">
		<div class="dropdown">
			<div tabindex="0" role="button" class="btn btn-ghost btn-circle">
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="h-5 w-5"
					fill="none"
					viewBox="0 0 24 24"
					stroke="currentColor"
				>
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M4 6h16M4 12h16M4 18h7"
					/>
				</svg>
			</div>
			<!-- svelte-ignore a11y-no-noninteractive-tabindex -->
			<ul
				tabindex="0"
				class="menu menu-sm dropdown-content bg-base-100 rounded-box z-[1] mt-3 w-52 p-2 shadow"
			>
				<li><a href="/" data-sveltekit-reload>Homepage</a></li>
				<li><a href="/FAQs">FAQs</a></li>
				<li><a href="/Pricing">Pricing</a></li>
			</ul>
		</div>
	</div>
	<div class="navbar-end">
		<a href="/" data-sveltekit-reload class="btn btn-ghost text-xl">ITVE</a>
	</div>
</div>
