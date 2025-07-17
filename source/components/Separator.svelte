<script>
  export let middleChar = "";
  let wWidth = 0;
  $: sepWidth = 150;
  $: renderString = "═".repeat(sepWidth / 5);
  $: console.log(renderString);
</script>

<div
  bind:clientWidth={wWidth}
  class="flex items-center justify-center w-full w-screen-max h-0.5 mt-10 text-white/50 animate-pulse rounded-full"
  style="animation-duration:2.5s"
>
  {renderString}
  {middleChar}
  {renderString}
</div>
