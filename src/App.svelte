<script>
  import "./app.css";
  var bouncingText = "public\u00A0\u00A0beta!";
</script>

<main>
  <div class="flex justify-start items-center">
    <h1 class="ml-15 mt-20 font-semibold text-4xl text-shadow-lg/75">
      direc-tuit
    </h1>
    <div class="flex flex-row ml-2.5 mt-10 italic text-xs text-yellow-200">
      {#each bouncingText.split("") as character, i}
        <span
          class="m-0.125 animate-bounce text-xl"
          style="animation-delay: {(i % 3) * 100}ms"
        >
          {character}
        </span>
      {/each}
    </div>
  </div>

  <p class="ml-15 mb-5 mt-1 text-gray-400 text-shadow-lg/90 italic text-2xs">
    [dəˈrɛkt tə ɪt]
  </p>
  <p class="ml-15 italic text-sm">
    a simple way to visualize files in your terminal
  </p>
</main>
