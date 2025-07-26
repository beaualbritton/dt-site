<script>
import demo1GIF from '../static/demo1.gif';
import demo2GIF from '../static/demo2.gif';
import screenShot1 from '../static/screenshot1.png'; 
import screenShot2 from '../static/screenshot2.png'; 
</script>
<div class="mt-2 font-semibold text-8xl text-shadow-lg/50 flex flex-row">
  <h1>demo</h1>
  {#each "!!!" as character, i}
  <span
    class="m-0.125 sync-bounce text-8xl"
    style="animation-delay: {(i % 5) * 100}ms; animation-duration: 2s;"
  >
    {character}
  </span>
{/each}
</div>
<section class = "w-3xl m-auto">
  <div class = "flex justify-center px-2">
    <div class="grid grid-cols-2 gap-4 place-items-center w-fit m-auto">  
      <img style="image-rendering: auto;"class = "w-fit rounded-xl shadow-lg hover:animate-pulse" src={demo1GIF} alt="Demo">
      <img style="image-rendering: auto;"class = "w-fit rounded-xl shadow-lg hover:animate-pulse" src={screenShot2} alt="Demo">
      <img style="image-rendering: auto;"class = "w-fit rounded-xl shadow-lg hover:animate-pulse" src={screenShot1} alt="Demo">
      <img style="image-rendering: auto;"class = "w-fit rounded-xl shadow-lg hover:animate-pulse" src={demo2GIF} alt="Demo">
    </div>
  </div>

</section>
