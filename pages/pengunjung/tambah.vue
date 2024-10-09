<template>
  <div class="container-fluid content">
    <div class="row">
      <div class="col-lg-8">
        <h2 class="text-center my-4">KATEGORI OBAT</h2>
        <form>
          <div class="mb-3 row">
              <label for="" class="col-sm-2 col-form-label">NAMA OBAT :</label>
              <div class="col-sm-10">
                <input type="text" class="form-control" id="">
              </div>
        </div>
        <div class="mb-3 row">
              <label for="" class="col-sm-2 col-form-label">MANFAAT :</label>
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
              <label for="" class="col-sm-2 col-form-label">JUMLAH OBAT :</label>
              <div class="col-sm-10">
                <input type="text" class="form-control" id="">
              </div>
          </div>
          <div class="text-end">
            <button type="submit" class="btn btn-white btn-lg m-2 px-5">AMBIL</button> 
            <button type="submit" class="btn btn-white btn-lg m-2 px-5">KEMBALI</button>         
          </div>
        </form>
      </div>
      <div class="col-lg-4">
        <img src="~/assets/img/obat.png" class="rounded" alt="obat">
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
.btn{
  background: #d9d9d9;
}
</style>