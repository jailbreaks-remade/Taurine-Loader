<script lang="ts">
    import ToggleButton from "./ToggleButton.svelte";
    export let text: string;
    export let toggleButton: boolean = false;
    let border: string;
    import arrow from '../assets/arrow.png'

    if(text === "Credits"){
        border = "border-none"
    } else {
        border = "border-gray-600"
    }
</script>
<div class={"flex w-full items-center p-3 border-b-[0.25px] " + border}>
    <div>{text}</div>
    <div class="flex-1"></div>
    {#if toggleButton}
        <ToggleButton/>
    {:else}
        <img class="w-[2.5vw] mr-2" alt="arrow" src={arrow}/>
    {/if}
  </div>