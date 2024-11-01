<template>
  <div class="content">
    <div class="row px-5">
      <div class="col-1 p-5">
        <NuxtLink to="/Halkedua/" class="btn btn-light center rounded-4 px-5 fw-bold">Kembali</NuxtLink>
      </div>
      <div class="row my-2 justify-content-center">
        <div class="col-5">
          <div class="bg-light rounded-5">
            <h1 class="text-center">OBAT-OBATAN DAN ALAT</h1>
          </div>
        </div>
      </div>
      
      <div class="row my-5 bg-pink justify-content-center rounded-4">
        <div class="col">
          <div class="row">
            <div class="col text-center my-4">
              <NuxtLink class="btn btn-light btn-lita">OBAT</NuxtLink> 
            </div>
          </div>
          <div class="row">
            <div v-for="(obat, i) in obats" :key="i" class="col my-4">
              <NuxtLink :to="`/pengunjung/obat/${obat.id}`" class="btn btn-light btn-lita">{{ obat.nama }}</NuxtLink>
            </div>
          </div>
        </div>
        <div class="col">
          <div class="row">
            <div class="col text-center my-4">
              <NuxtLink class="btn btn-light btn-lita">ALAT</NuxtLink>
            </div>
          </div>
          <div class="row">
            <div v-for="(alat, i) in alats" :key="i" class="col text-center my-4">
              <NuxtLink :to="`/pengunjung/${alat.id}`" class="btn btn-light btn-lita">{{ alat.nama }}</NuxtLink>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const supabase = useSupabaseClient()
const keyword = ref('')
const alats = ref([])
const obats = ref([])

const getAlat = async () => {
  const { data, error } = await supabase.from('data_alat').select()
  if(data) alats.value = data
}
const getObat = async () => {
  const { data, error } = await supabase.from('obat').select()
  if(data) obats.value = data
}

// const visitorFiltered = computed(() => {
//   return visitors.value.filter((b) => {
//       return (
//           b.nama?.toLowerCase().includes(keyword.value?.toLowerCase())
//       )
//   })
// })

onMounted(() =>{
  getAlat()
  getObat()
})
</script>


<style scoped>
.content {
  background-color: #B84F4F;
}

h1{
  color: #742626;
}

.bg-pink {
  background-color: #F9A6A6;
}
.bg-light {
  background-color: #d9d9d9 !important;
}

.btn-lita{
  width: 20rem;
}

.contect{
  background: #F9A6A6;
}
@import url('https://fonts.googleapis.com/css2?family=Irish+Grover&display=swap');
.container-fluid {
  /* background: url("~/assets/img/OBAT-OBATAN 1.png"); */
  background-size: cover;
  width: 100%;
}
td {
  color: white;
  border: 1px solid #fff;
  background-color: rgba(255, 255, 255, 0);
}

h2{
  color: white;
  font-family: "Irish Grover", system-ui;
}

.bi-caret-left-fill {
  margin-left: 20px;
}

</style> 

          
      