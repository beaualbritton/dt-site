<script>
  var bouncingText = "public\u00A0beta!";
</script>

<section>
  <div class="flex justify-start items-center">
    <h1 class="font-semibold text-5xl text-shadow-lg/50">direc-tuit</h1>
    <div class="flex flex-row ml-2.5 mb-10 italic text-md text-yellow-200">
      {#each bouncingText.split("") as character, i}
        <span
          class="m-0.125 animate-bounce text-2xl"
          style="animation-delay: {(i % 3) * 100}ms; animation-duration: 1.75s;"
        >
          {character}
        </span>
      {/each}
    </div>
  </div>

  <p
    class="mb-5 mt-1 text-gray-400 text-shadow-lg/75 italic font-light text-md"
  >
    [dəˈrɛkt tə ɪt]
  </p>
  <p class="font-medium text-lg">
    a simple way to visualize files in your terminal.
  </p>
</section>
