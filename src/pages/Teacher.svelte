<script>
  import { t } from "../i18n";

  import {fade} from 'svelte/transition'

</script>

<div class="container d-flex mt-5 pt-5 justify-content-center">
  <div class="d-flex flex-column justify-content-center text-justify p-5">
    <p>
        {$t('about')[0]}
    </p>
    {#if $t('about')[1]}
    <p>
        {$t('about')[1]}
    </p>
    {/if}
  </div>
  <img src="images/roman.jpg" alt="Roman outside" class="shadow mb-5" in:fade={{duration: 1000}}/>
</div>

<style>
  img {
    max-width: 50%;
    object-fit: cover;
  }
  @media only screen and (max-width: 768px) {
    img {
      max-width: 80%;
      margin: 2rem 0;
    }
    .container {
      flex-wrap: wrap;
    }
  }
</style>
