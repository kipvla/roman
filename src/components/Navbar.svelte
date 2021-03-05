<script>
  import { link } from "svelte-routing";
  import { onMount } from "svelte";

  onMount(() => {
    function classToggle() {
      console.log("toggled");
      const navs = document.querySelectorAll(".navbar-items");
      navs.forEach((nav) => nav.classList.toggle("show"));
    }
    document
      .querySelectorAll(".nav-item")
      .forEach((item) => item.addEventListener("click", classToggle));
  });

  let large = true;
  if (window.innerWidth < 769) {
    large = false;
  }

  // translate
  import translations from "../translations";
  import { dict, locale, t } from "../i18n";

  $: languages = Object.keys(translations);

  $: dict.set(translations);
</script>

<nav
  class="navbar navbar-expand-lg navbar-light fixed-top justify-content-between"
  id="mainNavbar"
>
  <a class="navbar-brand" href="/"
    >Roman {#if large} Yearian, violin {/if}</a
  >
  <button
    class="navbar-toggler"
    type="button"
    data-toggle="collapse"
    data-target="#navbarSupportedContent"
    aria-controls="navbarSupportedContent"
    aria-expanded="false"
    aria-label="Toggle navigation"
  >
    <span class="navbar-toggler-icon" />
  </button>

  <nav
    class="collapse navbar-collapse navbar-items"
    id="navbarSupportedContent"
  >
    <ul class="navbar-nav mr-auto">
      <li class="nav-item">
        <a class="nav-link" href="/about" use:link>{$t("navbar")[0]} </a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="/projects" use:link>{$t("navbar")[1]} </a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="/media" use:link>{$t("navbar")[2]} </a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="/teacher" use:link>{$t("navbar")[3]} </a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="/contact" use:link>{$t("navbar")[4]} </a>
      </li>
    </ul>
  </nav>
  <select bind:value={$locale}>
    {#each languages as lang}
      <option value={lang}
        ><span id="lang">{lang}</span>
        {#if lang === "en"}
          &#127482;&#127480;
        {:else}
          &#127474;&#127485;
        {/if}
      </option>
    {/each}
  </select>
</nav>

<style>
  .navbar {
    background-color: transparent;
  }
  #navbarSupportedContent {
    float: right;
  }
  select {
    background: transparent;
    border: none;
  }
  select:hover {
    border: 1px solid black;
  }
  #lang {
    visibility: invisible;
  }
  @media only screen and (max-width: 768px) {
    .nav-link {
      color: black !important;
    }
    #mainNavbar {
      background-color: rgba(255, 255, 255, 0.6);
    }
  }
</style>
