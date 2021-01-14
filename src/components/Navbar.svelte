<script>
  import { link } from 'svelte-routing';
</script>

<nav class="navbar navbar-expand-lg navbar-light">
  <div class="container d-flex justify-content-between w-100">
    <a class="navbar-brand" href="/">Roman Yearian</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse w-auto" id="navbarSupportedContent">
      <ul class="navbar-nav mr-auto">
        <li class="nav-item">
          <a class="nav-link" href="/about" use:link>About</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/projects" use:link>Projects</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/media" use:link>Media</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/teacher" use:link>Teacher</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/contact" use:link>Contact</a>
        </li>
      </ul>
      <!-- <form class="form-inline my-2 my-lg-0">
        <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
        <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
      </form> -->
    </div>
  </div>
  </nav>

  <!-- <div id="mainNavbar" class="navbar navbar-expand-lg d-flex align-items-baseline">
    <a href="/" class="nav-link navbar-link-brand"><h4>Roman Yearian</h4></a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <nav class="collapse navbar-collapse d-flex" id="navbarSupportedContent"> 
      <ul class="navbar-nav">
        <a href="/about" use:link class="nav-link active">about</a>
        <a href="/projects" use:link class="nav-link">projects</a>
        <a href="/media" use:link class="nav-link">media</a>
        <a href="/teacher" use:link class="nav-link">teacher</a>
        <a href="/contact" use:link class="nav-link">contact</a>
      </ul>
    </nav>
  </div> -->