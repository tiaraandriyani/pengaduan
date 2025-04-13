<template>
    <div class="container-fluid p-0">
      <nav class="navbar navbar-expand-lg navbar-dark custom-navbar">
        <div class="container-fluid d-flex align-items-center">
          <!-- Logo -->
          <a class="navbar-brand d-flex align-items-center" href="#">
            <img src="/assets/logobpn.png" alt="Logo" class="logo" />
          </a>
  
          <!-- Button Toggle (Mobile) -->
          <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarNav"
          >
            <span class="navbar-toggler-icon"></span>
          </button>
  
          <!-- Menu -->
          <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
            <ul class="navbar-nav me-4">
              <li class="nav-item mx-3">
                <nuxt-link to="/" class="nav-link fw-bold">HOME</nuxt-link>
              </li>
              <li class="nav-item mx-3">
                <nuxt-link to="/pengaduan" class="nav-link fw-bold">PENGADUAN</nuxt-link>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </div>
  </template>
  
  <style scoped>
  /* Warna latar belakang navbar */
  .custom-navbar {
    background-color: #C4C4C4 !important; /* Warna abu-abu sesuai gambar */
    min-height: 80px;
    padding: 10px 0;
  }
  
  /* Ukuran logo */
  .logo {
    max-height: 80px;
  }
  
  /* Warna teks navbar + Hapus underline */
  .nav-link {
    text-decoration: none !important;
    font-size: 18px;
    color: black !important;
  }
  
  .nav-link:hover {
    color: #555 !important;
  }
  
  /* Jarak antar menu agar sesuai gambar */
  .nav-item {
    margin-right: 20px;
  }
  </style>
  