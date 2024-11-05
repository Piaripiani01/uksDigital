<template>
  <div class="container-fluid content">
    <div class="row">
      <div class="col-lg-8">
        <h2 class="text-center my-4">KATEGORI OBAT</h2>
        <form>
          <div class="mb-3 row">
              <label for="" class="col-sm-2 col-form-label">NAMA OBAT :</label>
              <div class="col-sm-10">
                <p type="text" class="form-control" id="">{{ obat.nama }}</p>
              </div>
        </div>
        <div class="mb-3 row">
              <label for="" class="col-sm-2 col-form-label">MANFAAT :</label>
              <div class="col-sm-10">
                <p type="text" class="form-control" id="">{{ obat.deskripsi }}</p>
              </div>
          </div>
          <div class="mb-3 row">
              <label for="" class="col-sm-2 col-form-label">JENIS OBAT :</label>
              <div class="col-sm-10">
                <p type="text" class="form-control" id="">{{ obat.jenis_obat?.nama }}</p>
              </div>
          </div>
          <div class="mb-3 row">
              <label for="" class="col-sm-2 col-form-label">JUMLAH OBAT :</label>
              <div class="col-sm-10">
                <p type="text" class="form-control" id="">{{ obat.jumlah }}</p>
              </div>
          </div>
          <div class="text-end">
            <!-- <button type="submit" class="btn btn-white btn-lg m-2 px-5 fw-bold">AMBIL</button> 
            <button type="submit" class="btn btn-white btn-lg m-2 px-5 fw-bold">KEMBALI</button> -->
            <NuxtLink to="/pengunjung/obat" class="btn btn-white btn-lg m-2 px-5 fw-bold">kembali</NuxtLink>
            <input type="button" class="btn btn-white btn-lg m-2 px-5 fw-bold" @click="kurangiObat" value="Ambil">
          </div>
        </form>
      </div>
      <div class="col-lg-4">
        <img src="~/assets/img/obat.png" class="rounded" alt="obat">
      </div>
    </div>
  </div>
</template>
<script setup>
const supabase = useSupabaseClient()
const route = useRoute()
const obat = ref([])

async function getDataObat() {
  const {data} = await supabase.from('obat').select(`*, jenis_obat(*)`).eq('id', route.params.id)
  .maybeSingle()
  if(data) obat.value = data
}

async function kurangiObat() {
  obat.value.jumlah -= 1
}

onMounted(() => {
  getDataObat()
})
</script>
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