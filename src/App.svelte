<script>
  import "./app.css";
  var bouncingText = "public beta!";
  console.log("public beta!".split(""));
  function bounceChar(char) {
    if (char === " ") return "\u00A0\u00A0";
    return char;
  }
</script>

<main>
  <div class="flex justify-start items-center">
    <h1 class="ml-15 mt-30 mb-5 font-semibold text-4xl">direc-tuit</h1>
    <div class="flex flex-row ml-2.5 mt-20 italic text-xs text-yellow-200">
      {#each bouncingText.split("") as character, i}
        <p class="m-0.125 animate-bounce" style="animation-delay: {i * 75}ms">
          {bounceChar(character)}
        </p>
      {/each}
    </div>
  </div>

  <p class="ml-15 italic text-sm">
    a simple way to visualize files in your terminal
  </p>
</main>
