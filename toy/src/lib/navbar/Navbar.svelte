<script lang="ts">
	export let pathname: string;
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
		<a href={link.path} class="navbar-link" class:active={pathname === link.path}>{link.name}</a>
	{/each}
</nav>

<style lang="postcss">
	.navbar {
		@apply  flex w-full justify-around py-2;
		.navbar-link {
			@apply text-sm h-10 px-6 font-semibold rounded-md border border-slate-200 text-slate-900 pt-2;
			&.active {
				@apply bg-black text-slate-100 font-bold;
			}
		}
	}
</style>
