<script>
	
	import { page } from '$app/stores';
	

	let navOpen = false
	function handleNav() {
		navOpen = !navOpen;
		

		
// 		navWidth === 0 ? navWidth = 40 : navWidth = 0;
	}
</script>

<header>
	<div class="darker" class:bodybg={navOpen}></div>
	<div class="corner">
		<a sveltekit:prefetch href="/">
			<img src="/images/logo.svg" alt="Welcome" />
		</a>
	</div>
	<div class="navToggle"  class:change={navOpen} on:click={handleNav}>
		<div></div><div></div><div></div>
	</div>
	<nav class:open={navOpen}>
		
		<ul>
			<li class:drop={navOpen} on:click={handleNav}
				>Features
				<ul>
					<li class:active={$page.url.pathname === '/todo'}>
						<a sveltekit:prefetch href="/todo">ToDo</a>
					</li>
					<li class:active={$page.url.pathname === '/calendar'}>
						<a sveltekit:prefetch href="/calendar">Calendar</a>
					</li>
					<li class:active={$page.url.pathname === '/reminders'}>
						<a sveltekit:prefetch href="/reminders">Reminders</a>
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

		
</header>
<style lang="scss">
	// Progect Colors
	$white: hsl(0, 0%, 98%);
	$medium-gray: hsl(0, 0%, 41%);
	$almost-black: hsl(0, 0%, 8%);
	header {
    display: flex;
    padding: 1.2rem 1rem;
    justify-content: space-between;
		.darker {
			display: none;
			
		}
		.bodybg {
			display: block;
				position: absolute;
				width: 100vw;
				height: 100vh;
				background: rgba(0,0,0,0.6);
				top: 0;
				left: 0;
				z-index: 1;
			}
		nav {
			display: none;
		}
		.open {
			position: absolute;
			right: 0;
			top: 0;
			z-index: 10;
			transition: all 0.5s;
			height: 100vh;
			width: 240px;
			display: flex;
			background-color: $white;
			transition: all ease-in-out .3s;
			
		}
		.navToggle {
			cursor: pointer;
			z-index: 100;
			position: relative;
			margin-right: 2rem;
			transition: all 1s ease-in-out;
			div:first-child{
				display: block;
				width: 2rem;
				height: 2px;
				background: $almost-black;
				position: absolute;
			}
			div:nth-child(2) {
				display: block;
				width: 2rem;
				height: 2px;
				background: $almost-black;
				position: absolute;
				top: 9px
			}
			div:nth-child(3) {
				display: block;
				width: 2rem;
				height: 2px;
				background: $almost-black;
				position: absolute;
				top: 18px;
				}
			}
		
		.change {
			div:first-child{
				transform-origin:center right;
				transform: rotate(-45deg);
			}
			div:nth-child(2) {
				display: none;
				
			}
			div:nth-child(3) {
				transform-origin: center right;
				transform: rotate(45deg);
				top: 22px;
				}
			&::after {
				content: '';
				width: 100vw;
				height: 100vh;
				background-color: rgba(0,0,0,0.4);
				z-index: 1;
			}	
		}
}

</style>