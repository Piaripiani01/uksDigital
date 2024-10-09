<template>
  <div class="content">
    <div class="row px-5">
      <div class="col-1 p-5">
        <NuxtLink class="btn btn-light">KEMBALI</NuxtLink>
      </div>

      <div class="row my-2 justify-content-center">
        <div class="col-5">
          <div class="bg-light rounded-5">
            <h1 class="text-center">OBAT-OBATAN DAN ALAT</h1>
          </div>
        </div>
      </div>
      
      <div class="row my-5 bg-pink justify-content-center">
        <div class="col">
          <div class="row">
            <div class="col text-center my-4">
              <NuxtLink class="btn btn-light btn-lita">OBAT</NuxtLink> 
            </div>
          </div>
          <kapas class="row">
            <div class="col text-center my-4">
              <NuxtLink to="/paracetamol" class="btn btn-light btn-lita">paracetamol</NuxtLink>
            </div>
            <div class="col text-center my-4">
              <NuxtLink to="/betadine" class="btn btn-light btn-lita">betadine</NuxtLink>
            </div>
          </kapas>
          <div class="row">
            <div class="col text-center my-4">
              <NuxtLink to="/alkohol" class="btn btn-light btn-lita">alkohol</NuxtLink>
            </div>
            <div class="col text-center my-4">
              <NuxtLink to="/opistan" class="btn btn-light btn-lita">opistan</NuxtLink>
            </div>
          </div>
        </div>
        <div class="col">
          <div class="row">
            <div class="col text-center my-4">
              <NuxtLink class="btn btn-light btn-lita">ALAT</NuxtLink>
            </div>
          </div>
          <kapas class="row">
            <div class="col text-center my-4">
              <NuxtLink to="/hansaplast" class="btn btn-light btn-lita">hansaplast</NuxtLink>
            </div>
            <div class="col text-center my-4">
              <NuxtLink to="/kapas" class="btn btn-light btn-lita">kapas</NuxtLink>
            </div>
          </kapas>
          <div class="row">
            <div class="col text-center my-4">
              <NuxtLink to="/tensi" class="btn btn-light btn-lita">tensi</NuxtLink>
            </div>
            <div class="col text-center my-4">
              <NuxtLink to="/oksigen" class="btn btn-light btn-lita">oksigen</NuxtLink>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// const supabase = useSupabaseClient()
// const keyword = ref('')
// const visitors = ref([])

// const getPengunjung = async () => {
//   const { data, error } = await supabase.from('pengunjung').select(`*, keanggotaan(*), keperluan(*)`)
//   .ilike('nama', `%${keyword.value}%`)
//   if(data) visitors.value = data
//   visitors.value = data
// }

// const visitorFiltered = computed(() => {
//   return visitors.value.filter((b) => {
//       return (
//           b.nama?.toLowerCase().includes(keyword.value?.toLowerCase())
//       )
//   })
// })

// onMounted(() =>{
//   getPengunjung()
// })
</script>


<style scoped>
.content {
  background: #B84F4F;
}

.bg-pink {
  background-color: #F9A6A6;
}
.bg-light {
  background-color: #d9d9d9 !important;
}

.btn-lita{
  width: 10rem;
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

          
      
