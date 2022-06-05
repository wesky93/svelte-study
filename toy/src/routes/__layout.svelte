<script lang="ts">
	import { page } from '$app/stores';

	import '../app.css';

	type Path = {
		path: string;
		name: string;
	};
	const navs: Path[] = [
		{ path: '/', name: 'home' },
		{ path: '/about', name: 'about' },
		{ path: '/todo', name: 'todo' }
	];
</script>

<nav class="navbar">
	{#each navs as link}
		<a href={link.path} class="navbar-link" class:active={$page.url.pathname === link.path}
			>{link.name}</a
		>
	{/each}
</nav>
<slot />

<style lang="postcss">
	.navbar {
		@apply bg-slate-100 flex w-full px-8 justify-around;
		.navbar-link {
			@apply hover:text-blue-300 text-blue-700 h-10 pt-2;
			&.active {
				@apply text-purple-600;
			}
		}
	}
</style>
