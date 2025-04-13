<template>
  <div class="container mt-5">
    <h5 class="text-center fw-bold mb-4">RIWAYAT PENGADUAN</h5>
    <div class="table-responsive">
      <table class="table table-bordered">
        <thead class="table-secondary">
          <tr>
            <th>No</th>
            <th>Nama Pengadu</th>
            <th>Tgl/bln/thn</th>
            <th>Alamat</th>
            <th>NIK/KTP</th>
            <th>Permasalahan</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(visitor, i) in visitors" :key="i">
            <td>{{ i + 1 }}.</td>
            <td>{{ visitor.nama }}</td>
            <td>{{ formatTanggal(visitor.tgl) }}</td>
            <td>{{ visitor.alamat }}</td>
            <td>{{ visitor.nik }}</td>
            <td>{{ visitor.uraian }}</td>
          </tr>
        </tbody>
      </table>
    </div>

    <!-- Tombol Kembali -->
    <div class="mt-3">
      <nuxt-link to="/pengaduan" class="btn custom-button">Kembali</nuxt-link>
    </div>
  </div>
</template>

<script setup>
const supabase = useSupabaseClient()
const visitors = ref([])

const getPengaduan = async () => {
  const { data, error } = await supabase.from('PENGADUAN').select(`*`)
    .order('id', { ascending: false })
  if (data) visitors.value = data
}

const formatTanggal = (tgl) => {
  const date = new Date(tgl)
  const day = String(date.getDate()).padStart(2, '0')
  const month = String(date.getMonth() + 1).padStart(2, '0')
  const year = date.getFullYear()
  return `${day}-${month}-${year}`
}

onMounted(() => {
  getPengaduan()
})
</script>

<style>
.table th, .table td {
  vertical-align: middle;
  text-align: center;
}
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
