<script>
    import storeData from "../store/store.js"

    let toggleDarkMode;

    storeData.subscribe(value => {
        toggleDarkMode = value
    })

    let toggleTab = 1

    const funcToggle = (index) => {
        toggleTab = index
    }
</script>

<div class={`box-tabs ${toggleDarkMode && "box-tabs-dark"}`}>
    <div class="selectors">
        <div on:click={() => funcToggle(1)} class={`selector ${toggleDarkMode ? "s1-dark" : "s1"}`}>Formule $</div>
        <div on:click={() => funcToggle(2)}  class="selector">Formule $$$</div>
    </div>

    {#if toggleTab === 1}
        <div class="contenu">
            <h2>Contenu 1</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Porro repudiandae aperiam, facere tempore at suscipit minima fuga ea totam obcaecati saepe illo quo natus dolor.</p>
        </div>
    {:else}
        <div class="contenu">
            <h2>Contenu 2</h2>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ullam, quod asperiores! Vero tempore a necessitatibus magnam placeat vel sapiente et quis distinctio atque! Reiciendis, ducimus!</p>
        </div>
    {/if}

    
    
</div>

<style>
    .box-tabs {
        border: 1px solid #333;
        max-width: 500px;
        margin: 100px auto
    }
    .box-tabs-dark {
        border: 1px solid #f1f1f1;
    }
    .selectors {
        display: flex;
    }
    .selector {
        cursor: pointer;
        width: 50%;
        height: 70px;
        line-height: 70px;
        text-align: center;
        font-size: 1.5rem;
        color: #fff;
        background-color: crimson;
    }
    .selector:hover {
        background: rgb(241,58,95);
    }
    .s1 {
        border-right: 1px solid #333;
    }
    .s1-dark {
        border-right: 1px solid #f1f1f1;
    }
    .contenu {
        min-height: 230px;
        height: auto;
        padding: 25px;
    }
</style>