<script lang="ts">
	import * as config from '$lib/config'
	import { page } from '$app/stores'
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, DarkMode } from 'flowbite-svelte'

	$: activeUrl = $page.url.pathname
	let activeClass =
		'text-md font-bold text-orange-600 dark:text-orange-600 dark:hover:text-orange-600 hover:text-orange-600 hover:border-orange-600'
	let nonActiveClass =
		'font-bold  text-md dark:text-white dark:hover:text-orange-600 hover:text-orange-600'
</script>

<Navbar color="none" class="w-full z-20 top-0 left-0">
	<NavBrand href="/">
		<span
			class="self-center whitespace-nowrap text-xl font-bold dark:text-white dark:hover:text-orange-600 hover:text-orange-600 transition-colors duration-300 hover:border-b-2 border-transparent hover:border-orange-600"
		>
			{config.title}
		</span>
	</NavBrand>

	<NavHamburger />

	<NavUl {activeUrl} {activeClass} {nonActiveClass}>
		<NavLi href="/" active={true}>Home</NavLi>
		<NavLi href="/about">About</NavLi>
		<NavLi href="/blog">Blog</NavLi>
	</NavUl>
</Navbar>
