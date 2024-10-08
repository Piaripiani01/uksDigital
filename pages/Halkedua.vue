<template>
  <div class="container-fluid p-0">
      <div class="row justify-content-center py-5">
          <div class="col-lg-5">
            <nuxt-link to="/pengunjung/tambah" style="text-decoration: none;">
                <div class="card bg-pengunjung rounded-5">
                    <div class="card-body">
                        <h3 class="text-center" pt-5 style="margin-top: 80px;">Daftar pemantauan kesehatan / CATATAN</h3>
                    </div>
                </div> 
                </nuxt-link>
          </div>

          <div class="col-lg-5">
                <div class="card bg-buku rounded-5">
                    <div class="card-body">
                        <h3 class="text-center" style="margin-top: 80px;">Obat obatan dan alat</h3>
                    </div>
                </div>
          </div>
      </div>

      <div class="row justify-content-center gy-3 py-5">
          
          <div class="col-lg-5">
              <nuxt-link to="/pengunjung" style="text-decoration: none;">
                  <div class="card pengunjung rounded-5">
                      <div class="card-body">
                          <h1 class="text-center" style="margin-top: 80px;">Laporan</h1>
                      </div>
                  </div>
              </nuxt-link>
          </div>
      </div>
  </div>
</template>

<script setup>

</script>

<style scoped>
.container-fluid {
  /* padding: 0;
  margin: 0; */
  background-color: #B84F4F;
}

.card {
  height: 250px;
  box-shadow: 1px 1px 10px hsl(0, 0%, 100%)
}

.card.bg-pengunjung {
  background: url('../assets/img/UKS.png') no-repeat center center;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
}

.card.bg-buku {
  background: url('../assets/img/OBAT.png') no-repeat center center;
  background-size: cover;
}

.pengunjung {
  background: url('../assets/img/LAPORAN.png') no-repeat center center;
  background-size: cover;
  color: white;

}
h2 {
  color: #742626;
  font-family: "Irish Grover", system-ui;
}

h3 {
  color:#742626;
}

h1 {
  color:#742626;
}

.row {
  gap: 80px;
}
</style>