<template>
  <div class="container-fluid content">
    <div class="row">
      <div class="col-lg-8">
        <h2 class="text-center my-4">TAMBAH OBAT</h2>
        <form>
          <div class="mb-3 row">
              <label for="" class="col-sm-2 col-form-label">NAMA OBAT :</label>
              <div class="col-sm-10">
                <input type="text" class="form-control" id="">
              </div>
        </div>
        <div class="mb-3 row">
              <label for="" class="col-sm-2 col-form-label">JENIS OBAT :</label>
              <div class="col-sm-10">
                <input type="text" class="form-control" id="">
              </div>
          </div>
          <div class="mb-3 row">
              <label for="" class="col-sm-2 col-form-label">JUMLAH ALAT :</label>
              <div class="col-sm-10">
                <input type="text" class="form-control" id="">
              </div>
          </div>
          <div class="mb-3 row">
              <label for="" class="col-sm-2 col-form-label">EXPIRED :</label>
              <div class="col-sm-10">
                <input type="text" class="form-control" id="">
              </div>
          </div>
          <div class="text-center">
            <button type="submit" class="btn btn-white btn-lg rounded-5 px-5 fw-bold">TAMBAHKAN</button>       
          </div> 
        </form>
      </div>
    </div>
  </div>
</template>

<style scoped>
img {
    height: 100px;
  
}
.content {
  background: #B84F4F;
  height: 100vh;
}
label, h2 {
  color: white;
  font-weight: 700;
}
.btn{
  background: #d9d9d9;
}
</style>