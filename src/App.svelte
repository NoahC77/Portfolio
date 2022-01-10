<script>
	import Button from './Button.svelte'
	import Navbar from './Navbar.svelte'
	import Sidebar from './Sidebar.svelte'

	let pic = './ProfilePicture.png'
	let pic2 = './article.jfif'
	let open = false;
	export let name;

</script>



<main>
	<img src={pic} class=right>
	<h1>Noah</h1>
	<h1>Castetters</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	<Button><a href="https://github.com/NoahC77">Github</a></Button>
	<Button>noahcastetter@gmail.com</Button>


	<Navbar bind:sidebar={open}/>
	<Sidebar bind:open/>
	
	<img src={pic2} style="float: right; width: 30%; height 200px; padding: 20px; background-color: #93c64e;">
	<div class="#about">This webpage is to showcase my expierence as a computer scientist. C++ and Java are the langauges I'm most proffecient with. I've used Java and C++ with git to version control and publish several projects to team members. Primarily my developer environment is vim with bash on Windows 10 WSL 2. Lastly I've worked with Gatsby, Svelte.js, SLURM, and CentOS</div>
</main>

<svelte:head>
  <link href="https://unpkg.com/tailwindcss@^1.0/dist/tailwind.min.css" rel="stylesheet"/>
</svelte:head>

<style>
	@import 'https://unpkg.com/@responsive-ui/button@latest/lib/index.css';

	:global(body){
		padding: 0;
	}
	
	.right {
		float: right;
		border-radius: 50%;
	}
	
	div {
		color: #ffaccc;
		font-family: Courier New;
		font-size: 3em;

	}
	main {
		background-color: #93c64e;
		text-align: left;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ffaccc;
		text-transform: uppercase;
		font-family: Courier New;
		font-size: 14em;
		font-weight: 100;
	}

	a {
		color: white;	
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
