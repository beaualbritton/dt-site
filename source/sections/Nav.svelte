<script lang="ts">
 let navList : String[] = ["Demo","Download", "About",];

  
</script>


<div class = "mt-10 flex flex-items justify-center">
  {#each navList as buttonName, i}
  <button class = "px-8 pt-1 bg-black/10 rounded-lg text-lg font-bold">{buttonName}</button>
  {/each}
</div>
