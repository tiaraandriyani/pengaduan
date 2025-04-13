<template>
    <div>
  
      <div class="container my-3">
        <!-- Judul -->
        <div class="text-center mb-5">
          <h4 class="fw-bold title">Persyaratan Pengaduan Kasus Pertanahan</h4>
          <h5 class="fw-semibold subtitle">(Sengketa dan Konflik)</h5>
        </div>
  
        <!-- Grid Persyaratan -->
        <div class="row justify-content-center">
          <div class="col-4">
            <h6 class="fw-bold">Perorangan</h6>
            <p>a) Fotokopi Bukti Identitas Diri</p>
            <p>b) Surat kuasa dan fotokopi identitas dari pemberi dan penerima kuasa apabila dikuasakan</p>
          </div>
  
          <div class="col-4">
            <h6 class="fw-bold">Badan Hukum</h6>
            <p>a) Fotokopi akta pendirian/perubahan terakhir</p>
            <p>b) Surat kuasa direksi</p>
            <p>c) Fotokopi identitas pemberi dan penerima kuasa apabila dikuasakan</p>
          </div>
  
          <div class="col-4">
            <h6 class="fw-bold">Kelompok Masyarakat</h6>
            <p>a) Fotokopi bukti identitas diri anggota kelompok masyarakat</p>
            <p>b) Surat kuasa dari seluruh anggota kelompok masyarakat dengan dilampiri fotokopi identitas penerima kuasa apabila dikuasakan</p>
          </div>
        </div>

        <div class="row justify-content-evenly" style="margin-top: 50px;">
          <div class="col-4">
            <h6 class="fw-bold">Instansi Pemerintah</h6>
            <p>Fotokopi bukti identitas diri pegawai atau pejabat yang berwenang disertai Surat Tugas atau Surat Kuasa dari Instansi yang bersangkutan.</p>
          </div>
  
          <div class="col-4">
            <h6 class="fw-bold">Kementerian/Kantor Wilayah/Kantor Pertanahan</h6>
            <p>Surat laporan dari pimpinan unit kerja atau satuan kerja yang bersangkutan.</p>
          </div>
        </div>
  
        <!-- Tombol Ajukan di sebelah kanan -->
        <div class="d-flex justify-content-end mt-5">
            <nuxt-link to="/form" class="btn custom-button">Ajukan</nuxt-link>
        </div>
      </div>
    </div>
</template>
  
<style scoped>
/* Judul */
.title {
  font-size: 22px;
  font-weight: bold;
}

.subtitle {
  font-size: 18px;
}

/* Grid Styling */
h6 {
  font-size: 16px;
  margin-bottom: 8px;
}

p {
  font-size: 14px;
  margin-bottom: 5px;
}

/* Button Styling */
.custom-button {
  background-color: #b0b0b0;
  border: none;
  color: black;
  font-weight: bold;
  font-size: 16px;
  width: 120px;
  border-radius: 8px;
}

.custom-button:hover {
  background-color: #a0a0a0;
}
</style>
