<script>
	import { page } from '$app/stores';
	
</script>

<header>
	<div class="corner">
		<a sveltekit:prefetch href="/">
			<img src="/images/logo.svg" alt="Welcome" />
		</a>
	</div>

	<nav>
		
		<ul>
			<li class:active={$page.url.pathname === '/features'}>
				<a sveltekit:prefetch href="/features">Features</a>
				<ul>
					<li class:active={$page.url.pathname === '/features/todo'}>
						<a sveltekit:prefetch href="/features/todo">ToDo</a>
					</li>
				</ul>
			</li>
			<li class:active={$page.url.pathname === '/company'}>
				<a sveltekit:prefetch href="/company">Company</a>
			</li>
			<li class:active={$page.url.pathname === '/careers'}>
				<a sveltekit:prefetch href="/careers">Careers</a>
			</li>
			<li class:active={$page.url.pathname === '/about'}>
				<a sveltekit:prefetch href="/about">About</a>
			</li>
		</ul>
		
	</nav>

	<div class="corner">
		<!-- TODO put something else here? github link? -->
	</div>
</header>