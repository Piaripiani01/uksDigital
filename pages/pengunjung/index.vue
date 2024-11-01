<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-lg-12">
        <div class="row d-flex justify-content-center">
          <h2 class="Titl text-center my-4 rounded-5">LAPORAN</h2>
        </div>
        <div class="my-3">
          <input type="search" class="form-control form-control-lg rounded-5" placeholder="Search...">
        </div>
        <div class="my-3 text-light">Menampilkan 1 dari 1</div>
        <table class="table">
          <thead>
            <tr>
              <td>NO</td>
              <td>NAMA</td>
              <td>KELAS</td>
              <td>HARI/TANGGAL/JAM</td>
              <td>KELUHAN</td>
              <td>RIWAYAT</td>
              <td>TINDAKAN</td>
              <td>KETERANGAN</td>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(siswa, i) in siswa" :key="siswa.id">
              <td>{{ i + 1 }}</td>
              <td>{{ siswa.id_siswa.nama }}</td>
              <td>{{ siswa.id_siswa.tingkat }} {{ siswa.id_siswa.jurusan }} {{ siswa.id_siswa.kelas }}</td>
              <td>{{ siswa.hari }} {{ siswa.tanggal }} {{ siswa.jam }}</td>
              <td>{{ siswa.keluhan }}</td>
              <td>{{ siswa.tindakan }}</td>
              <td>{{ siswa.keterangan }}</td>
              <td>-</td>
            </tr>
          </tbody>
        </table>
        <div class="text-end">
            <!-- <button to="/Halkedua"   type="submit" class="btn btn-lg center rounded-4 px-5 fw-bold">Kembali</button>        -->
            <NuxtLink to="/Halkedua" type="submit" class="btn btn-lg center rounded-4 px-5 fw-bold">Kembali</NuxtLink>
          </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const supabase = useSupabaseClient()
const siswa = ref([])

const getPemeriksaan = async () => {
  const { data, error } = await supabase.from('pemeriksaan')
  .select(`*, id_siswa(nama, tingkat, jurusan, kelas)`)
  if(data)siswa.value = data
}

// const visitorFiltered = computed(() => {
//       return visitors.value.filter((b) => {
//       return(
//         b.nama?.toLowerCase().includes(keyword.value?.toLowerCase())
//       )
//     })
// })

onMounted(() =>{
    getPemeriksaan()
})
</script>


<style scoped>
.container-fluid {
  background-color: #BC5959;
  height: 100vh;
}
.btn {
  background-color: #D9D9D9;
  color: #742626;
  width: 170px;
}
h2{
  color: #742626;
  background-color: #D9D9D9;
}

.Titl {
  width: 20rem;
}
th, td {
  border: 1px solid #fff;
  background: transparent;
  color: white;
}
</style>
