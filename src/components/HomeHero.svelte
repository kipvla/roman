<script>
  import {fade} from 'svelte/transition'
</script>

<div class="hero" in:fade={{duration:1000}}/>

<style>
  .hero {
    background-image: url("/images/bigbend.jpeg");
    background-size: cover;
    height: 800px;
  }
  @media only screen and (max-width: 768px) {
    .hero {
      background-position: 74% center;
    }
  }
</style>
