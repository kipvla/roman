<script>
  import { t } from "../i18n";

  import {fade} from 'svelte/transition'

</script>

<div class="container d-flex mt-5 pt-5 justify-content-center">
  <div class="d-flex flex-column justify-content-center py-3 py-md-0">
    <p>
        {$t('teaching')[0]}
    </p>
    {#if $t('teaching')[1]}
    <p>
        {$t('teaching')[1]}
    </p>
    {/if}
  </div>
  <img src="images/roman.jpg" alt="Roman outside" class="shadow" in:fade={{duration: 1000}}/>
</div>

<style>
  img {
    max-width: 50%;
    object-fit: cover;
    margin-bottom: 2rem;
  }
  @media only screen and (max-width: 768px) {
    img {
      max-width: 80%;
      order: -1;
      margin-bottom: 0;
    }
    .container {
      flex-wrap: wrap;
    }
  }
</style>
