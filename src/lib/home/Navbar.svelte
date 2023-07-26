<script>
	import { page } from '$app/stores';
	import { SquareSlash } from 'lucide-svelte';
	let navs = [
		{
			name: '/',
			link: '/'
		},
		{
			name: 'Blogs',
			link: '/blogs'
		},
		{
			name: 'About',
			link: '/about'
		}
	];
	$: activePage = $page.route.id;
	$: console.log(activePage);
</script>

<div class="navbar bg-base-100 md:px-20">
	<div class="navbar-start">
		<div class="dropdown">
			<label tabindex="0" class="btn btn-ghost lg:hidden">
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="h-5 w-5"
					fill="none"
					viewBox="0 0 24 24"
					stroke="currentColor"
					><path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M4 6h16M4 12h8m-8 6h16"
					/></svg
				>
			</label>
			<ul
				tabindex="0"
				class="menu menu-sm dropdown-content mt-3 z-[1] p-2 shadow bg-base-100 rounded-box w-52"
			>
				{#each navs as nav}
					<li>
						<a href={nav.link}>{nav.name}</a>
					</li>
				{/each}
			</ul>
		</div>
		<a
			class="btn btn-ghost normal-case text-xl bg-blue-50 border border-slate-800 hover:border-slate-800 hover:bg-blue-100 font-bold"
			href="/"><span><SquareSlash /></span>Delusion</a
		>
	</div>
	<div class="navbar-end hidden lg:flex">
		<ul class="menu menu-horizontal px-1">
			{#each navs as nav}
				<li>
					<a
						href={nav.link}
						class="hover:bg-slate-800 hover:text-white bg-zinc-50 border mx-1 border-slate-800
						{activePage === nav.link ? 'bg-green-100 ' : ''}">{nav.name}</a
					>
				</li>
			{/each}
		</ul>
	</div>
</div>
