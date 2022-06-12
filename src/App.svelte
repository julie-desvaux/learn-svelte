<script>
	import Navbar from "./components/Navbar.svelte"
	import Button from "./components/Button.svelte"
	import Modal from "./components/Modal.svelte"
	import Tabs from "./components/Tabs.svelte"
	import storeData from "./store/store.js"

	let toggleModal = false;
	let toggleDarkMode

	storeData.subscribe(value => {
		toggleDarkMode = value
	})

	const toggleFunc = () => {
		toggleModal=!toggleModal
	}
</script>

<Navbar />
<div class={`container ${toggleDarkMode ? "go-dark" : 'go-light'}`}>
	<Button />
	<h1>Title</h1>
	<div class="flex">
		<button on:click={toggleFunc}>Modal</button>
	</div>
	
	{#if toggleModal}
		<Modal on:close={toggleFunc}/>
	{/if}
	
	<div>
		<Tabs />
	</div>
</div>


<style>
	.container {
		width: 100%;
		height: auto;
		min-height: calc(100vh - 70px);
		transition: color 0.2s ease-in, background-color 0.2s ease-in;
	}
	h1 {
		padding: 25px 80px;
		text-align: center;
	}
	.flex {
		width: 100%;
		display: flex;
		justify-content: center;
	}
	.flex button {
		padding: 10px 20px;
		border: 1px solid #333;
		border-radius: 20px; 
	}
</style>