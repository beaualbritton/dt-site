<script>
  export let middleChar = "";
  let wWidth = 0;
  $: sepWidth = 150;
  $: renderString = "═".repeat(sepWidth / 5);
</script>

<button on:click bind:clientWidth={wWidth} class="flex items-center justify-center w-full w-screen-max mt-10 text-white/60 sync-pulse rounded-full" style="animation-duration:2s">
  {renderString} <div class="text-3xl text-white/90 sync-bounce" style="animation-duration: 3s;"> {"\u00A0"+middleChar+"\u00A0"} </div> {renderString}
</button>
