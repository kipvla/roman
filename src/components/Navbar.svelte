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
    // document.querySelector('.navbar-items').addEventListener('click', classToggle);
  });

  let large = true;
  if (window.innerWidth < 769){
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
  <a class="navbar-brand" href="/">Roman {#if large} Yearian, violin {/if}</a>
  <!-- {info.navbar[0]} -->
  <button
    class="navbar-toggler"
    type="button"
    data-toggle="collapse"
    data-target="#navbarSupportedContent"
    aria-controls="navbarSupportedContent"
    aria-expanded="false"
    aria-label="Toggle navigation">
    <span class="navbar-toggler-icon" />
  </button>

  <nav
    class="collapse navbar-collapse navbar-items"
    id="navbarSupportedContent"
  >
    <ul class="navbar-nav mr-auto">
      <li class="nav-item">
        <a class="nav-link" href="/about" use:link>{$t('navbar')[0]}
        </a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="/projects" use:link>{$t('navbar')[1]}
        </a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="/media" use:link>{$t('navbar')[2]}
        </a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="/teacher" use:link>{$t('navbar')[3]}
        </a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="/contact" use:link>{$t('navbar')[4]}
        </a>
      </li>
      <!-- <li class="nav-item dropdown">
        <a class="nav-link dropdown-toggle" href="/" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
          Dropdown
        </a>
        <div class="dropdown-menu" aria-labelledby="navbarDropdown">
          <a class="dropdown-item" href="/">Action</a>
          <a class="dropdown-item" href="/">Another action</a>
          <div class="dropdown-divider"></div>
          <a class="dropdown-item" href="/">Something else here</a>
        </div>
      </li>
      <li class="nav-item">
        <a class="nav-link disabled" href="/">Disabled</a>
      </li> -->
    </ul>
    <!-- <form class="form-inline my-2 my-lg-0">
      <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
      <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
    </form> -->
  </nav>
  <select bind:value={$locale}>
    {#each languages as lang}
      <option value={lang}>{lang}</option>
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
  @media only screen and (max-width: 768px) {
    .nav-link {
      color: black!important;
    }
  }
</style>
