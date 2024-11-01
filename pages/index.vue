<template>
  <div class="content">
    <div class="d-flex justify-content-between px-5">
      <img src="@/assets/img/logoPMR.png" alt="" width="130" height="150">
      <div class="text-center pt-5">
        <p>Selamat Datang di</p>
        <h1>UKS SEKOLAH DIGITAL</h1>
        <h3 class="bg-body-secondary p-1">Smkn 4 Tasikmalaya</h3>
      </div>
      <div class="stars">
        <img src="@/assets/img/Star 1.svg" alt="" width="80">
        <img src="@/assets/img/Star 1.svg" alt="" width="80">
      </div>
    </div>
    <div class="contect d-flex flex-column justify-content-center align-items-center">
      <img src="@/assets/img/jam.png" alt="" width="200">
      <NuxtLink to="/Halkedua/" class="bg-body-secondary rounded-3">@masuk website</NuxtLink>
    </div>
    <div class="position-relative">
      <img src="@/assets/img/footerhome.svg" alt="" class="img_footer">
      <div class="position-absolute bottom-0 end-0 text-end">
        <h4>SMKN4 Tasikmalaya</h4>
        <h4 class="m-0">JL.depok.sukamenak.purbaratu</h4>
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: 'layoutUtama'
})
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Irish+Grover&display=swap');

p {
  color: white;
  font-family: "Irish Grover", system-ui;
  font-weight: 400;
  font-style: normal;
  font-size: 30px;
}

h1 {
  color: white;
  font-family: "Irish Grover", system-ui;
  font-weight: 500;
  font-style: normal;
  font-size: 40px;
}

h3 {
  color: #742626;
  font-family: "Irish Grover", system-ui;
  font-weight: 500;
  font-style: normal;
  font-size: 30px;
}

.content {
  background: #F28787;
}

h4 {
  color: #742626;
  }

.card {
  height: 30px;
  box-shadow: 1px 1px 10px #726a6a;
}

.card.bg-pengunjung {
  background-repeat: no-repeat;
  background-position: center center;

}

.text {
  padding-left: 250px;
}

.img_footer {
  width: 100%;
}
</style>
