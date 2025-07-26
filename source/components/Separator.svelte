<script>
  export let middleChar = "";
  $: renderString = "═".repeat(10);
</script>

<button on:click class="flex items-center justify-center m-auto text-md lg:text-3xl text-white/60 sync-pulse rounded-full" style="animation-duration:2s">
  {renderString} <div class="text-3xl text-white/90 sync-bounce" style="animation-duration: 3s;"> {"\u00A0"+middleChar+"\u00A0"} </div> {renderString}
</button>
