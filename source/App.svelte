<script>
  import Separator from "./components/Separator.svelte";
  import Header from "./sections/Header.svelte";
  import About from "./sections/About.svelte";
  import Demo from "./sections/Demo.svelte"
  import Download from "./sections/Download.svelte";
  let sectionArray= [Header,Demo,Download, About];
  $:currentSectionIndex = 0;
  $:animationFlag = false;
  $:animationDuration = 500;//ms
  async function navigateSectionDown()
  {
    animationFlag = true;

    await new Promise(p => setTimeout(p, animationDuration));
    if(currentSectionIndex < sectionArray.length)
    {
      ++currentSectionIndex;
    }
    animationFlag = false;
  }
  async function navigateSectionUp()
  {
    animationFlag = true;
    await new Promise(p => setTimeout(p, animationDuration));
    if(currentSectionIndex > 0)
    {
      --currentSectionIndex;
    }
    animationFlag = false;
  }
  $: currentSection = sectionArray[currentSectionIndex];
</script>

<main class ="flex items-center flex-col h-screen">
  <div class = "flex items-center justify-center h-screen flex-col">
    <div class={`inline-block transition-all ease-in-out duration-${animationDuration} ${animationFlag ? 'opacity-0 translate-y-6' : 'opacity-100 translate-y-0'}`} style="animation-duration: 3.5s;">
      {#if currentSectionIndex > 0}
      <Separator on:click={navigateSectionUp} middleChar="▲"/>
      {/if}
      <div >
        <svelte:component  this = {currentSection}/>
      </div>
      {#if currentSectionIndex < sectionArray.length-1}
      <Separator on:click={navigateSectionDown} middleChar="▼" />
      {/if}
      {#if currentSectionIndex >= sectionArray.length-1}
      <Separator middleChar="♥"/>
      {/if}
    </div>
      
  </div>
</main>
