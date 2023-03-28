<script>
    import {
        Button,
        Header,
        HeaderNav,
        SkipToContent,
    } from "carbon-components-svelte";
    import ThemeSelectorComponent from "./ThemeSelectorComponent.svelte";

    export let page = "Home"
</script>

<Header company="Hedgehog Burrow">
    <svelte:fragment slot="skip-to-content">
        <SkipToContent/>
    </svelte:fragment>
    <HeaderNav>
        <Button class="navigation_button" on:click={() => {page = "Home"; console.log(page)}}>Home</Button>
        <Button class="navigation_button" on:click={() => {page = "Buy"; console.log(page)}}>Buy</Button>
        <Button class="navigation_button" on:click={() => {page = "About"; console.log(page)}}>About</Button>
    </HeaderNav>

    <ThemeSelectorComponent/>
</Header>


<style>
    :global(.bx--btn.navigation_button) {
        background: #161616;
        display: flex;
        align-items: center;
        margin: auto;
    }
</style>