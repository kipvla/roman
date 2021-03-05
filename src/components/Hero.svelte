<script>
  import { t } from "../i18n";

  import { fade } from "svelte/transition";
</script>

<div
  class="container-fluid d-flex justify-content-center align-items-center mt-5"
  id="main"
>
  <div class="py-5">
    <div class="pr-md-5 pl-md-3">
      <p>{$t("about")[0]}</p>
      {#if $t("about")[1]}
        <p>{$t("about")[1]}</p>
      {/if}
      {#if $t("about")[2]}
        <p>{$t("about")[2]}</p>
      {/if}
    </div>
  </div>
  <img
    class="shadow my-1"
    src="images/roman.jpg"
    alt=""
    in:fade={{ duration: 1000 }}
  />
</div>

<style>
  img {
    width: 50%;
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
