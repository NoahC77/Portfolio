<script>
	import Logo from './Logo.svelte'
	import Hamburger from './Hamburger.svelte'
	import Menu from './Menu.svelte'
	
	export let sidebar = false
</script>

<header class="flex justify-between green-200 p-2 items-center text-gray-600">
	<nav class="flex">
		<!-- Side navigation bar disabled for version 1 -->
		<!-- <Hamburger bind:open={sidebar}/> -->
		<Logo/>	
	</nav>
	
	<Menu/>
</header>
