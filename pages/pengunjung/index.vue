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
        <div class="my-3 text-muted">Menampilkan 1 dari 1</div>
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
            <tr>
              <td>1.</td>
              <td>PIA RIPIANI</td>
              <td>XII PPLG 3</td>
              <td>Kamis, 25 september 2024, 23.31.00</td>
              <td>PUSING</td>
              <td>-</td>
              <td>TIDAK</td>
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
