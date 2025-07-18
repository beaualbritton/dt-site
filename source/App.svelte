<script>
  import Separator from "./components/Separator.svelte";
  import Header from "./sections/Header.svelte";
  import About from "./sections/About.svelte";
  $:sectionArray= [Header,About];
  $:currentSectionIndex = 0;
  function navigateSectionDown()
  {
    if(currentSectionIndex < sectionArray.length)
    {
      ++currentSectionIndex;
    }
  }
  function navigateSectionUp()
  {
    if(currentSectionIndex > 0)
    {
      --currentSectionIndex;
    }
  }
  $: currentSection = sectionArray[currentSectionIndex];
</script>

<main class="flex items-center justify-center h-screen flex-col">
  <div class="inline-block">
    {#if currentSectionIndex > 0}
    <Separator on:click={navigateSectionUp} middleChar="▲"/>
    {/if}
    <svelte:component this = {currentSection}/>
    {#if currentSectionIndex < sectionArray.length}
    <Separator on:click={navigateSectionDown} middleChar="▼" />
    {/if}
  </div>
</main>
