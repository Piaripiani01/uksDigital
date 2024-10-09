<template>
  <div class="container-fluid content">
    <div class="row">
      <div class="col-lg-10">
        <h2 class="text-center my-4">ISI DAFTAR PEMANTAUAN KESEHATAN SISWA</h2>
        <form>
          <div class="mb-3 row">
            <label for="" class="col-sm-2 col-form-label">NAMA:</label>
            <div class="col-sm-10">
              <input type="text" class="form-control ic rounded-5" id="">
            </div>
          </div>
          <div class="mb-3 row">
            <label for="" class="col-sm-2 col-form-label">KELAS:</label>
              <div class="col-sm-10">
              <div class="row d-flex">
                <div class="col-md-4">
                <select class="form-control ic form-control-lg form-select rounded-5 mb-2">
                  <option value="text">TINGKAT</option>
                  <option value="X">X</option>
                  <option value="XI">XI</option>
                  <option value="XII">XII</option>
                </select>
                </div>
            <div class="col-md-4">
                <select class="form-control ic form-control-lg form-select rounded-5 mb-2">
                  <option value="">JURUSAN</option>
                  <option value="PPLG">PPLG</option>
                  <option value="TJKT">TJKT</option>
                  <option value="TBSM">TBSM</option>
                  <option value="DKV">DKV</option>
                  <option value="TOI">TOI</option>
                </select>
              </div>
              <div class="col-md-4">
                <select class="form-control ic form-control-lg form-select rounded-5 mb-2">
                  <option value="">KELAS</option>
                  <option value="1">1</option>
                  <option value="2">2</option>
                  <option value="3">3</option>
                  <option value="4">4</option>
                </select>
              </div>
            </div>
          </div>
          <div class="mb-3 row">
            <label for="" class="col-sm-2 col-form-label">HARI, TANGGAL, JAM:</label>
            <div class="col-sm-10">
              <div class="row d-flex">
              <div class="col-md-4">
                <select class="form-control ic form-control-lg form-select rounded-5 mb-2">
                  <option value="">Hari</option>
                  <option value="Senin">Senin</option>
                  <option value="Selasa">Selasa</option>
                  <option value="Rabu">Rabu</option>
                  <option value="Kamis">Kamis</option>
                  <option value="Jum'at">Jum'at</option>
                </select>
              </div>
              <div class="col-md-4">
                <input type="date" class="form-control ic rounded-5" id="">
              </div>
              <div class="col-md-4">
                <input type="text" class="form-control ic rounded-5" id="">
                </div>
              </div>
            </div>
            </div>
        <div class="mb-3 row">
            <label for="" class="col-sm-2 com-lal-forbel">KELUHAN/GEJALA:</label>
            <div class="col-sm-10">
            <input type="text" class="form-control ic rounded-5" id="">
            </div>
        </div>
        </div>
        <div class="mb-3 row">
              <label for="" class="col-sm-2 col-form-label">RIWAYAT PENYAKIT:</label>
              <div class="col-sm-10">
                <input type="text" class="form-control ic rounded-5" id="">
              </div>
          </div>
          <div class="mb-3 row">
              <label for="" class="col-sm-2 col-form-label">TINDAKAN/PENANGANAN:</label>
              <div class="col-sm-10">
                <input type="text" class="form-control ic rounded-5" id="">
              </div>
          </div>
          <div class="mb-3 row">
              <label for="" class="col-sm-2 col-form-label">KETERANGAN:</label>
              <div class="col-sm-10">
                <input type="text" class="form-control ic rounded-5" id="">
              </div>
          </div>
          <div class="text-end">
            <NuxtLink to="/pengunjung" type="submit" class=" btn btn-outline-danger center rounded-4 px-5 fw-bold">Kirim</NuxtLink>   
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
label, h2 {
  color: white;
  font-weight: 700;
}
.btn {
  background-color: hsl(0, 0%, 85%);
}

.ic{
  background-color: #C3A8A8;
}
</style>
