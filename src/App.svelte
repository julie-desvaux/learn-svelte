<script>
	import Modal from "./components/Modal.svelte"
	import Tabs from "./components/Tabs.svelte"
	let toggle = false;

	const toggleFunc = () => {
		toggle=!toggle
	}
</script>

<h1>Title</h1>
<button on:click={toggleFunc}>Modal</button>

{#if toggle}
	<Modal on:close={toggleFunc}/>
{/if}

<div>
	<Tabs />
</div>

<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quae vitae molestias unde veritatis consequatur porro delectus tempore incidunt repellendus labore repudiandae eaque necessitatibus, cupiditate quam tenetur officiis fugiat error, aspernatur sint vel corporis assumenda dicta quos. Nihil rerum, necessitatibus cupiditate, unde eum libero cumque, officia illum dicta veritatis reiciendis eius reprehenderit hic debitis aspernatur commodi quae nam sit. Ipsum libero provident dolorum, quam fugiat iure et laboriosam eum aut magni quia saepe officia aliquam a, recusandae animi minima in porro explicabo voluptatem neque suscipit nesciunt hic non? Quia maiores explicabo sunt alias consequuntur eum omnis quasi maxime cupiditate aspernatur laborum voluptatem sint odio voluptates sed, facere similique architecto. Delectus quia animi vero perspiciatis, facere deserunt placeat nulla odio nam adipisci? Corporis neque ipsum ut blanditiis officia atque quae possimus velit ex in, excepturi nam molestias earum exercitationem consequatur unde dolorum commodi enim ea inventore facere? Vitae animi aperiam asperiores voluptatem deserunt! Pariatur eveniet aliquam vel culpa odio excepturi, amet, non accusamus dicta voluptatum nulla! Et tenetur eligendi dignissimos. Deleniti quod neque quas eos modi id cupiditate doloremque sequi obcaecati consectetur. Dolorem pariatur nesciunt assumenda officiis ipsa dicta expedita id in. Perspiciatis rem eos cupiditate est in, saepe veniam placeat, consequuntur odio quis pariatur quas numquam provident, qui suscipit! Incidunt facere, natus aliquam debitis, dolore aliquid iusto nostrum perferendis ratione laudantium architecto quae ducimus ea illo libero amet molestiae sint doloremque laborum necessitatibus quisquam, saepe commodi. Porro molestiae quod officiis? Excepturi suscipit tenetur, dolor neque recusandae reprehenderit pariatur ipsam autem, sequi beatae laboriosam, placeat nesciunt itaque? Expedita, corrupti saepe. Ex, temporibus laborum alias debitis eius impedit ipsa tenetur, reprehenderit nemo in consectetur nisi, aliquid molestiae maiores porro! Illo quibusdam error consectetur assumenda natus! Voluptatum, quos excepturi veniam, magni numquam error facere voluptatem dolores reprehenderit, cumque cum laboriosam doloremque nulla cupiditate maiores.</p>

<style>
	
</style>