<script>
import demo1GIF from '../static/demo1.gif';
import demo2GIF from '../static/demo2.gif';
import screenShot1 from '../static/screenshot1.png'; 
import screenShot2 from '../static/screenshot2.png'; 
</script>

<section class = " max-w-xs lg:max-w-2xl m-auto text-start shadow-lg/75 p-4 lg:p-8 rounded-md mt-10 mb-10">
  <div class="flex flex-col justify-start text-start">
  <div class = "flex flex-row justify-start text-start">
    <h1 class="font-semibold text-7xl lg:text-9xl text-shadow-lg/50">demo</h1>
  {#each "!!!" as character, i}
  <span
    class="m-0.125 sync-bounce text-7xl lg:text-9xl text-shadow-lg/50 "
    style="animation-delay: {(i % 5) * 100}ms; animation-duration: 2s;"
  >
    {character}
  </span>
{/each}

  </div>
  <div class = "-mt-2.5 lg:-mt-5 flex justify-center px-2">
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-4 place-items-center m-auto">  
      <img style="image-rendering: auto;"class = " lg:w-full w-fit rounded-xl shadow-lg hover:animate-pulse" src={demo1GIF} alt="Demo">
      <img style="image-rendering: auto;"class = "hidden  lg:block w-fit rounded-xl shadow-lg hover:animate-pulse" src={screenShot2} alt="Demo">
      <img style="image-rendering: auto;"class = " w-fit rounded-xl shadow-lg hover:animate-pulse" src={screenShot1} alt="Demo">
      <img style="image-rendering: auto;"class = " w-fit rounded-xl shadow-lg hover:animate-pulse" src={demo2GIF} alt="Demo">
    </div>
  </div>

</div>

</section>
