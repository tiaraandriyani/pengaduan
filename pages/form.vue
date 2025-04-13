<template>
 <div class="container mt-5">
    <h5 class="text-center fw-bold mb-4">FORMULIR PENGADUAN</h5>
    <form @submit.prevent="kirimData">
      <div class="row g-3">
        <!-- Baris 1: Nama & NIK -->
        <div class="col-md-6">
          <input v-model="form.nama" type="text" class="form-control" name="nama" placeholder="Nama Pengadu" required>
        </div>
        <div class="col-md-6">
          <input v-model="form.nik"  type="text" class="form-control" name="nik" placeholder="Nomor Induk Kependudukan/KTP" required>
        </div>

        <!-- Baris 2: Tanggal + Alamat di kiri, Uraian di kanan -->
        <div class="col-md-6">
          <div class="row g-3">
            <div class="col-12">
              <input v-model="form.tgl"  type="date" class="form-control" name="tanggal" placeholder="Tanggal" required>
            </div>
            <div class="col-12">
              <input v-model="form.alamat"  type="text" class="form-control" name="alamat" placeholder="Alamat" required>
            </div>
          </div>
        </div>

        <div class="col-md-6">
          <textarea v-model="form.uraian" class="form-control" name="uraian" rows="4" placeholder="uraian singkat permasalahan" required></textarea>
        </div>

        <!-- Tombol -->
        <div class="col-12 text-end">
          <button type="submit" class="btn btn-secondary">KIRIM</button>
        </div>
      </div>
    </form>
  </div>
</template>
<script setup>
const supabase = useSupabaseClient()

const form = ref({
    nama: "",
    tgl:"",
    alamat:"",
    nik:"",
    uraian:"",
});

const kirimData = async () => {
    console.log(form.value)
    const { error } = await supabase.from("PENGADUAN").insert([form.value])
    if(!error) navigateTo("/riwayat")
    else throw error
}
</script>