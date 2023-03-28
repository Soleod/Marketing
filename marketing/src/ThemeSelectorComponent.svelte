<script>
    import {Button, Theme} from "carbon-components-svelte";
    import {BrightnessContrast} from "carbon-icons-svelte";

    let possibleThemes = {
        "Light": "g10",
        "Dark": "g80"
    }
    let theme = possibleThemes["Light"];

    function changeTheme() {
        theme === "g10" ? theme = possibleThemes["Dark"] : theme = possibleThemes["Light"];
    }
</script>

<Theme bind:theme/>
<div class="button_container">
    <Button iconDescription="Color" icon={BrightnessContrast} on:click={changeTheme}/>
</div>


<style>
    .button_container {
        margin-left: auto
    }
</style>