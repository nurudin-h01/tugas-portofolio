<template>
  <div class="home">
    <div class="container">
      <div class="row py-5">
        <div class="col-12 col-lg-8 d-flex">
            <div class="my-auto">
              <h1 class="text-start fw-bold" style="color: #645193ff;">Hello my name is Nurudin</h1>
              <p class="text-start">This is my portofolio Website</p>
            </div>
        </div>
        <div class="col-4 d-none d-lg-block">
          <img  alt="" class="img-fluid" src="../assets/2833678.jpg">
        </div>
      </div>
      <div>
        <h2 class="mt-5 mb-3 fw-bold" style="color: #645193ff;">This is my project</h2>
        <div class="row">
          <div v-for="(items, index) in image" :key="index" class="col-4">
            <div class="card mb-5">
              <img :src="items.images" class="card-img-top" alt="...">
              <div class="card-body">
                <h5 class="card-title fw-bold" style="color: #645193ff;">{{items.title}}</h5>
                <p class="card-text">{{items.desc}}</p>
                <router-link class="btn btn-outline-primary" :to="{name: 'Project', params: {project: items.title}}">Detail</router-link>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue';

export default {
  name: 'Home',
  data: () => ({
    profile: 'https://images.unsplash.com/photo-1518791841217-8f162f1e1131?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=800&q=60',
    image: [
      { images: 'img/nutziverse.png', title: 'Nutziverse', desc: 'Website untuk menghitung kebutuhan gizi sehari-hari' },
      { images: 'img/warungmama.png', title: 'WarungMama', desc: 'Website untuk menyediakan kebutuhan sehari-hari' },
      { images: 'img/umahbali.png', title: 'UmahBali', desc: 'Website untuk menyediakan informasi properti' },
    ],
  }),
};
</script>

<style>
.btn-outline-primary, .btn-outline-primary:hover, .btn-outline-primary:active, .btn-outline-primary:visited {
    color: #645193ff !important;
    border-color: #645193ff !important;
}
.btn-outline-primary:hover{
  background-color: #645193ff !important;
  color: white !important;
}
</style>
