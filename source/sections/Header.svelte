<script>
  var bouncingText = "public\u00A0beta!";
</script>

<section class = "w-3xl">
  <div class="flex justify-start items-center">
    <h1 class="font-semibold text-8xl text-shadow-lg/50">direc-tuit</h1>
    <div class="flex flex-row ml-2.5 mb-15 italic text-yellow-200">
      {#each bouncingText.split("") as character, i}
        <span
          class="m-0.125 animate-bounce text-4xl"
          style="animation-delay: {(i % 3) * 100}ms; animation-duration: 1.5s;"
        >
          {character}
        </span>
      {/each}
    </div>
  </div>

  <p
    class="-mt-5 mb-2 text-gray-400 text-shadow-lg/75 italic font-light text-lg"
  >
    [dəˈrɛkt tʊ ɪt]
  </p>
  <p class="font-bold text-2xl">
    a simple way to visualize files in your terminal.
  </p>
</section>
