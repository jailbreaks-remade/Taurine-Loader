<script lang="ts">
  let enabled: boolean = false;
  let bg: string = "bg-gray-200";
  let pos: string = "";
  

  const toggle = () => {
    enabled = !enabled;
    enabled ? bg = "bg-green-400" : bg = "bg-gray-200"
    enabled ? pos = "translate-x-5" : pos = "";
  }
</script>

<button on:click={toggle} class={bg + " rounded-full w-[3rem] transition-all focus:outline-none"}>
  <div class={"p-3.5 w-3.5 rounded-full h-3.5 bg-white shadow-xl transition-all " + pos}>&nbsp;</div>
</button>

<style>
</style>