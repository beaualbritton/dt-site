<script>
  export let middleChar = "";
  let wWidth = 0;
  $: sepWidth = 150;
  $: renderString = "═".repeat(sepWidth / 5);
</script>

<button on:click bind:clientWidth={wWidth} class="flex items-center justify-center w-full w-screen-max h-0.5 mt-10 text-white/60 animate-pulse rounded-full" style="animation-duration:2s">
  {renderString} <div class="text-3xl"> {middleChar} </div> {renderString}
</button>
