<template>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+Thai+Looped:wght@100&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css"> 
  <div>
        <nav class="navbar navbar-expand-lg bg-success">
  <div class="container-fluid">
    <a class="navbar-brand text-light" href="#">Navbar</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active text-light" aria-current="page" href="/">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link text-light" href="/about">about us</a>
        </li>
        <li class="nav-item">
          <a class="nav-link text-light" href="/limitmessage">Limit Message</a>
        </li>
        <li class="nav-item">
          <a class="nav-link text-light" href="/previewImage">Preview Image</a>
        </li>
      </ul>
      <form class="d-flex text-light" role="search">
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
        <button class="btn btn-outline-success" type="submit">Search</button>
      </form>
    </div>
  </div>
</nav>
    </div>
    <slot />

    <footer>
        <p><i class="bi bi-person-circle"> - Yaneesa Chaisuwan</i></p>
        <p><i class="bi bi-hospital"> - Thai-Austrian Technical College</i></p>
        <p><i class="bi bi-envelope-at"> - 66309010007@tatc.ac.th</i></p>
    </footer>
</template>
<style>
         footer {
            background-color: #e9f8d1;
            padding: 20px;
            text-align: center;
            position: fixed;
            left: 0;
            bottom: 0;
            width: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            font-family: 'IBM Plex Sans Thai Looped', sans-serif;
            font-size: 20px;
            color: #555;
            box-shadow: 0px -2px 10px rgba(2, 27, 11, 0.1);
        }
</style>