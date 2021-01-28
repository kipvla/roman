<script>
  import {fade} from 'svelte/transition'
</script>

<div class="hero" in:fade={{duration:1000}}/>

<style>
  .hero {
    background-image: url("/images/bigbend.jpeg");
    background-size: cover;
    background-position: 48% center;
    height: 800px;
  }
</style>
