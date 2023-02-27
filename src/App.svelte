<script lang="ts">
  import './app.css'
    import TableElement from './comp/TableElement.svelte';
    import Tablerow from './comp/Tablerow.svelte';
    import ToggleButton from './comp/ToggleButton.svelte';

    let jailbreaking: boolean = false;
    const runJB = () => {
      jailbreaking = true;
      setTimeout(() => {  jailbreaking = false; }, 3000);
    }
</script>

<main class="flex justify-center h-screen items-center flex-col mt-1.5 w-full">
    <h1 class="taurine w-full grid place-items-center p-5">TAURINE</h1>
    <div class="table rounded-2xl h-[37%] mb-10 w-[65%] mt-2 shadow-xl">
      <Tablerow toggleButton text="Enable Tweaks"/>
      <Tablerow toggleButton text="Restore RootFS"/>
      <Tablerow text="Themes"/>
      <Tablerow text="Settings"/>
      <Tablerow text="Credits"/>
    </div>
    <button on:click={runJB} class="jb-btn p-4 w-[65%] rounded-2xl shadow-xl">{#if jailbreaking}Jailbreaking...{:else}Jailbreak{/if}</button>
</main>