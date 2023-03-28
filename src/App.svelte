<script>
    import "carbon-components-svelte/css/all.css";
    import HomeComponent from "./HomeComponent.svelte";
    import HeaderComponent from "./HeaderComponent.svelte";
    import BuyComponent from "./BuyComponent.svelte";
    import AboutComponent from "./AboutComponent.svelte";

    let htmlContent = ''
    fetch('HedgehogGame.html').then(response => {
        console.dir(response)
        return response.text();
    }).then(html => {
        htmlContent = html
    })

    let page = "Home"
</script>

<main>
    <HeaderComponent bind:page={page}/>

    {#if page == "Home"}
        <HomeComponent/>
    {/if}
    {#if page == "Buy"}
        <BuyComponent/>
    {/if}
    {#if page == "About"}
        <AboutComponent/>
    {/if}
</main>

<style>
    :global(.bx--btn--primary) {

        border-width: 1px;
        border-style: solid;
        border-color: rgba(0, 0, 0, 0);
        background-color: var(--cds-interactive-01, #0f62fe);
        color: var(--cds-text-04, #ffffff);

    }

    :global(.bx--btn) {
        font-size: var(--cds-body-short-01-font-size, 0.875rem);
        font-weight: var(--cds-body-short-01-font-weight, 400);
        line-height: var(--cds-body-short-01-line-height, 1.28572);
        letter-spacing: var(--cds-body-short-01-letter-spacing, 0.16px);
        position: relative;
        display: inline-flex;
        max-width: 20rem;
        min-height: 3rem;
        flex-shrink: 0;
        align-items: center;
        justify-content: space-between;
        padding: 10px 30px;
        margin: 0;
        border-radius: 0;
        cursor: pointer;
        outline: none;
        text-align: left;
        text-decoration: none;
        transition: background 70ms cubic-bezier(0, 0, 0.38, 0.9), box-shadow 70ms cubic-bezier(0, 0, 0.38, 0.9), border-color 70ms cubic-bezier(0, 0, 0.38, 0.9), outline 70ms cubic-bezier(0, 0, 0.38, 0.9);
        vertical-align: top;
    }
</style>
