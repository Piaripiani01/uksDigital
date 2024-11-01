<template>
  <div class="container-fluid content">
    <div class="row">
      <div class="col-lg-8">
        <h2 class="text-center my-4">DATA ALAT</h2>
        <form>
          <div class="mb-3 row">
              <label for="" class="col-sm-2 col-form-label">NAMA ALAT :</label>
              <div class="col-sm-10">
                <p type="text" class="form-control" id="">{{ alat.nama }}</p>
              </div>
        </div>
        <div class="mb-3 row">
              <label for="" class="col-sm-2 col-form-label">KEGUNAAN :</label>
              <div class="col-sm-10">
                <p type="text" class="form-control" id="">{{ alat.kegunaan }}</p>
              </div>
          </div>
          <div class="mb-3 row">
              <label for="" class="col-sm-2 col-form-label">JUMLAH ALAT :</label>
              <div class="col-sm-10">
                <p type="text" class="form-control" id="">{{ alat.jumlah }}</p>
              </div>
          </div>
          <div class="text-end">
          </div>
          <div class="justify-content-end d-flex">
            <NuxtLink to="/utama" class="btn btn-white btn-lg m-2 px-5 fw-bold">kembali</NuxtLink>
            <input type="button" class="btn btn-white btn-lg m-2 px-5 fw-bold" @click="kurangiObat" value="Ambil">
          </div>  
        </form>
      </div>
    </div>
  </div>
</template>

<script setup>
const supabase = useSupabaseClient()
const route = useRoute()
const alat = ref([])

async function getDataAlat() {
  const {data} = await supabase.from('data_alat').select().eq('id', route.params.id)
  .maybeSingle()
  if(data) alat.value = data
}

async function kurangiObat() {
  obat.value.jumlah -= 1
}

onMounted(() => {
  getDataAlat()
})
</script>

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