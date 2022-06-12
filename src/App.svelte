<script>
	import Navbar from "./components/Navbar.svelte"
	import Modal from "./components/Modal.svelte"
	import Tabs from "./components/Tabs.svelte"
	let toggle = false;

	const toggleFunc = () => {
		toggle=!toggle
	}
</script>

<Navbar />

<h1>Title</h1>
<div class="flex">
	<button on:click={toggleFunc}>Modal</button>
</div>

{#if toggle}
	<Modal on:close={toggleFunc}/>
{/if}

<div>
	<Tabs />
</div>

<style>
	h1 {
		margin: 20px 0;
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