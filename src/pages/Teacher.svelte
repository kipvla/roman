<script>
  import { t } from "../i18n";
</script>

<div class="container d-flex mt-5 pt-5 justify-content-center">
  <div class="d-flex flex-column justify-content-center">
    <p>
        {$t('about')[0]}
    </p>
    {#if $t('about')[1]}
    <p>
        {$t('about')[1]}
    </p>
    {/if}
  </div>
  <img src="images/roman.jpg" alt="" />
</div>

<style>
  img {
    max-width: 50%;
  }
  @media only screen and (max-width: 768px) {
    img {
      max-width: 80%;
    }
    .container {
      flex-wrap: wrap;
    }
  }
</style>
