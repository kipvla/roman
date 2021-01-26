<script>
  import {t} from '../i18n'
</script>

<style>
    img {
        width:50%;
    }
  @media only screen and (max-width: 1023px) {
    #main {
      flex-flow: column wrap;
      padding-top: 2rem;
    }
    img {
        order: -1;
        width: 80vw;
        object-fit: cover;
    }
  }
</style>

<div class="container-fluid d-flex justify-content-center align-items-center mt-5" id="main">
    <div class="p-5">
        <!-- <h1 class="display-3 text-align-center justify-content-center">Hi! I'm Roman.</h1> -->
        <div class="">
          <p>{$t('about')[0]}</p>
          {#if $t('about')[1]}
          <p>{$t('about')[1]}</p>
          {/if}
          {#if $t('about')[2]}
          <p>{$t('about')[2]}</p>
          {/if}
        </div>
    </div>
    <img class="shadow" src="images/roman.jpg" alt="">
</div>