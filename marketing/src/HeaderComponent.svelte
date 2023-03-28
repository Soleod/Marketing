<script>
    import {
        Header,
        HeaderNav,
        HeaderNavItem,
        HeaderNavMenu,
        SkipToContent,
    } from "carbon-components-svelte";
    import ThemeSelectorComponent from "./ThemeSelectorComponent.svelte";

    let isSideNavOpen = false;
</script>

<Header company="Lorem Ipsum" bind:isSideNavOpen>
    <svelte:fragment slot="skip-to-content">
        <SkipToContent/>
    </svelte:fragment>
    <HeaderNav>
        <HeaderNavItem href="/" text="Home"/>
        <HeaderNavItem href="/" text="Buy"/>
        <HeaderNavItem href="/" text="About"/>
    </HeaderNav>

    <ThemeSelectorComponent/>
</Header>


<style>

</style>