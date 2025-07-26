<script>
  var bouncingText = "public\u00A0beta!";
</script>

<section class = "max-w-sm lg:max-w-2xl m-auto text-start shadow-lg/75 p-4 lg:p-8 rounded-md mb-10">
  <div class="flex items-center justify-start text-center">
    <h1 class="font-semibold text-7xl lg:text-9xl text-shadow-lg/50">direc-tuit</h1>
    <div class="flex flex-row mb-15 italic text-yellow-200">
      {#each bouncingText.split("") as character, i}
        <span
          class="m-0.125 animate-bounce text-3xl lg:text-5xl lg:-mt-5"
          style="animation-delay: {(i % 3) * 100}ms; animation-duration: 1.5s;"
        >
          {character}
        </span>
      {/each}
    </div>
  </div>

  <p
    class="max-w-fit text-center lg:text-start -mt-7.5 mb-2.5 lg:mb-5 text-gray-400 text-md lg:text-2xl text-shadow-lg/75"
  >
    [dəˈrɛkt tʊ ɪt]
  </p>
  <p class="font-bold text-xl lg:text-3xl">
    a simple way to visualize files in your terminal.
  </p>
</section>
