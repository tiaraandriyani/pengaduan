<template>
  <header class="hero">
    <div class="overlay">
      <div class="container d-flex flex-column align-items-center justify-content-center">
        <h1 class="hero-title">
          Kementerian Agraria dan Tata Ruang/ Badan Pertanahan Nasional
        </h1>
      </div>
    </div>
  </header>
</template>

<style scoped>
/* Hero Section */
.hero {
  position: relative;
  width: 100%;
  height: calc(100vh - 110px); /* Mengisi sisa layar setelah navbar */
  background: url('/assets/bg.jpg') center/cover no-repeat;
  
}

/* Overlay Transparan */
.overlay {
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5); /* Overlay agar teks lebih terbaca */
  display: flex;
  align-items: center; /* Pusatkan vertikal */
  justify-content: center; /* Pusatkan horizontal */
}

/* Pastikan container juga memenuhi area overlay */
.container {
  min-height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

/* Teks Hero */
.hero-title {
  color: white;
  font-size: 28px;
  font-weight: bold;
  text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.7);
  text-align: center;
  max-width: 80%;
}
</style>
