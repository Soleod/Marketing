<script>
    import "carbon-components-svelte/css/all.css";
    import ThemeSelector from "./ThemeSelectorComponent.svelte";
    import HeaderComponent from "./HeaderComponent.svelte";

    let htmlContent = ''
    fetch('HedgehogGame.html').then(response => {
        console.dir(response)
        return response.text();
    }).then(html => {
        htmlContent = html
    })
</script>

<main>
    <HeaderComponent/>

</main>

<style>

</style>
