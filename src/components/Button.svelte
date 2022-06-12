<script>
    import storeData from "../store/store.js"

    let toggleDarkMode;

    storeData.subscribe(value => {
        toggleDarkMode = value
    })

    const toggleScreen = () => {
        storeData.set(!toggleDarkMode)
    }
</script>

<button on:click={toggleScreen} class={`btn-toggle ${toggleDarkMode ? "go-light" : 'go-dark'}`} type="button">{toggleDarkMode ? "Go Light" : "Go Dark"}</button>

<style>
    .btn-toggle {
        width: 70px;
        height: 70px;
        border-radius: 50%;
        outline: none;
        position: absolute;
        top: 85px;
        right: 15px;
        cursor: pointer;
    }
</style>