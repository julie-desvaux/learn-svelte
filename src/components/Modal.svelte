<script>
    import {createEventDispatcher} from "svelte"
    const dispatch = createEventDispatcher();

    const closeModal = () => {
        dispatch('close' )
    }
</script>

<div on:click={closeModal} class="overlay"></div>
<div class="modal">
    <h2>Lorem ipsum dolor sit amet.</h2>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi earum quaerat, maiores at aliquam tempora non totam id, deleniti facere mollitia illo itaque deserunt veritatis.</p>
    <button on:click={closeModal} class="btn-danger">x</button>
</div>

<style>
    .overlay {
        position: fixed;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        background: rgba(0,0,0,0.3);
    }
    .modal {
        width: 500px;
        border: 1px solid #333;
        padding: 15px;
        background: white;
        position: fixed;
        top: 45%;
        left: 50%;
        transform: translate(-50%,-50%);
    }
    .btn-danger {
        position: absolute;
        top:5px;
        right: 5px;
        background: crimson;
        border: 1px solid lightgray;
    }
</style>