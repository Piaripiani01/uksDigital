<script setup>
const supabase = useSupabaseClient()
const form = ref({
  nama: "",
  hari: "",
  tanggal: "",
  jam: "",
  keluhan: "",
  riwayat: "",
  tindakan: "",
  keterangan: "",
})
const kelas = ref({
  tingkat: '',
  jurusan: '',
  kelas: ''
})
const students = ref([])

const getSiswa = async () => {
  const { data, error } = await supabase
  .from('siswa')
  .select('*')
  .eq('tingkat', kelas.value.tingkat)
  .eq('jurusan', kelas.value.jurusan)
  .eq('kelas', kelas.value.kelas)
  if (error) throw error
  if (data) students.value = data
}

async function tambahData() {
  const { data, error } = await supabase
    .from('pemeriksaan')
    .insert([form.value])
    .select()
  if(data) navigateTo ('/pengunjung')
}

watch(kelas.value, () => {
  if (kelas.value.tingkat && kelas.value.jurusan && kelas.value.kelas) {
    getSiswa()
  }
})
</script>

<template>
  <div class="container-fluid content">
    <div class="row justify-content-center">
      <div class="col-lg-10">
        <h2 class="text-center my-4">ISI DAFTAR PEMANTAUAN KESEHATAN SISWA</h2>
        <form @submit.prevent="tambahData">
          <div class="mb-3 row">
            <label for="" class="col-sm-2 col form-label">TINGKAT, JURUSAN, KELAS:</label>
            <div class="col-sm-10">
              <div class="row d-flex">
                <div class="col-md-4">
                  <select v-model="kelas.tingkat" class="form-control ic form-control-lg form-select rounded-5 mb-2">
                    <option disabled value="">Tingkat</option>
                    <option>X</option>
                    <option>XI</option>
                    <option>XII</option>
                  </select>
                </div>
                <div class="col-md-4">
                  <select v-model="kelas.jurusan" class="form-control ic form-control-lg form-select rounded-5 mb-2">
                    <option disabled value="">Jurusan</option>
                    <option>PPLG</option>
                    <option>TJKT</option>
                    <option>TSM</option>
                    <option>DKV</option>
                    <option>TOI</option>
                  </select>
                </div>
                <div class="col-md-4">
                  <select v-model="kelas.kelas" class="form-control ic form-control-lg form-select rounded-5 mb-2">
                    <option disabled value="">Kelas</option>
                    <option>1</option>
                    <option>2</option>
                    <option>3</option>
                    <option>4</option>
                  </select>
                </div>
              </div>
            </div>
          </div>

          <div class="mb-3 row">
            <label for="" class="col-sm-2 col form">NAMA:</label>
            <div class="col-sm-10">
              <select v-model="form.nama" :disabled="!kelas.tingkat || !kelas.jurusan || !kelas.kelas" class="form-control ic form-select rounded-5 text-dark">
                <option v-for="siswa in students" :key="siswa.id_siswa" :value="siswa.id_siswa">{{ siswa.nama }}</option>
              </select>
            </div>
          </div>
          
          <div class="mb-3 row">
            <label for="" class="col-sm-2 col form-label">HARI, TANGGAL, JAM:</label>
            <div class="col-sm-10">
              <div class="row d-flex">
                <div class="col-md-4">
                  <select v-model="form.hari" class="form-control ic form-control-lg form-select rounded-5 mb-2">
                    <option disabled value="">Hari</option>
                    <option value="Senin">Senin</option>
                    <option value="Selasa">Selasa</option>
                    <option value="Rabu">Rabu</option>
                    <option value="Kamis">Kamis</option>
                    <option value="Jum'at">Jum'at</option>
                  </select>
                </div>
                <div class="col-md-4">
                  <input v-model="form.tanggal" type="date" class="form-control ic rounded-5" id="">
                </div>
                <div class="col-md-4">
                  <input v-model="form.jam" type="time" class="form-control ic rounded-5" id="">
                </div>
              </div>
            </div>
          </div>
          <div class="mb-3 row">
            <label for="" class="col-sm-2 col form-label">KELUHAN / GEJALA:</label>
            <div class="col-sm-10">
              <input v-model="form.keluhan" type="text" class="form-control ic rounded-5" id="">
            </div>
          </div>
          <div class="mb-3 row">
            <label for="" class="col-sm-2 col form-label">RIWAYAT PENYAKIT:</label>
            <div class="col-sm-10">
              <input v-model="form.riwayat"type="text" class="form-control ic rounded-5" id="">
            </div>
          </div>
          <div class="mb-3 row">
            <label for="" class="col-sm-2 col form-label">TINDAKAN / PENANGANAN:</label>
            <div class="col-sm-10">
              <input v-model="form.tindakan" type="text" class="form-control ic rounded-5" id="">
            </div>
          </div>
          <div class="mb-3 row">
            <label for="" class="col-sm-2 col form-label">KETERANGAN:</label>
            <div class="col-sm-10">
              <input v-model="form.keterangan" type="text" class="form-control ic rounded-5" id="">
            </div>
          </div>
          <div class="text-end">
            <button type="submit" class=" btn btn-outline-danger center rounded-4 px-5 fw-bold">Kirim
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<style scoped>
img {
  height: 100%;
  margin-left: 50px;

}

.content {
  background: #B84F4F;
  height: 100vh;
}

label,
h2 {
  color: white;
  font-weight: 700;
}

.btn {
  background-color: hsl(0, 0%, 85%);
}

.ic {
  background-color: #C3A8A8;
}

.form-control {
  color: white;
}
</style>
