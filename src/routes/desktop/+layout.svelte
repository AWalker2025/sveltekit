<script>
  import { count, filter } from './store'
</script>

<div class ="options">
    <form>
      <p><b>Filter Results:</b></p>
     <label for="normal">
       <input type="radio" id="normal" name="fav_language" value="" bind:group={$filter}>Normal
     </label><br>
  
     <label for="greyscale">
          <input type="radio" id="greyscale" name="fav_language" value="grayscale" bind:group={$filter}>Greyscale
     </label><br>
  
     <label for="blur">
          <input type="radio" id="blur" name="fav_language" value="blur" bind:group={$filter}>Blur
     </label><br>
  
     <label for="both">
      <input type="radio" id="greyscale and blur" name="fav_language" value="grayscale&blur" bind:group={$filter}>Greyscale and Blur
  </label><br>
  </form>
  <div class="Counter">
    <p><b>Number of Photos Needed:</b></p>
    <input type="range" bind:value={$count} min=0 max=20 />
    <span>{ $count }</span>
  </div>
</div>

<slot />