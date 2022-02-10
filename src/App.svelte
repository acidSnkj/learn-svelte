<script>
	import About from "./components/About.svelte";
	import Text from "./components/Text.svelte";
	import Person from "./components/Person.svelte";
	import Skills from "./components/Skills.svelte";
import Input from "./components/Input.svelte";

	export let name;
	export let lastName;
	let svelteLogo = "../adeptus.png";
	const data = {
		name: "Adeptus",
		lastName: "Sororitas",
		age: 32
	};
</script>

<main>
	<h1>{name} {lastName} !</h1>
	<About />
	<Text anotherText="Otro text" />
	<Text />
	<Person {...data}   />
	<Skills />
	<Input />
	<img src={svelteLogo} alt="Svelte logo" />
</main>

<style>
	:global(body) {
		background-color: rgb(167, 39, 39);
		color: cyan;
	}
	:global(:root) {
		--theme-color: white;
	}

	:global(body.dark-mode) {
		background-color: steelblue;
		color: papayawhip;
	}

	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	main img {
		width: 30%
	}
	h1 {
		color: var(--theme-color);
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>