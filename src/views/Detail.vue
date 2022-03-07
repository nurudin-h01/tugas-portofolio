<template>
    <div class="container">
        <div v-if="detail === undefined">
            <h2 class="text-center mt-5 mb-3 fw-bold" style="color: #645193ff">Detail Project</h2>
            <div class="row mt-2">
            <div v-for="(items, index) in image" :key="index" class="col-4">
                <div class="card">
                <img :src="items.images2" class="card-img-top" alt="...">
                <div class="card-body">
                    <h5 class="card-title">{{items.title}}</h5>
                    <p class="card-text">{{items.desc}}</p>
                    <router-link class="btn btn-outline-primary" :to="{name: 'Project', params: {project: items.title}}">Detail</router-link>
                </div>
                </div>
            </div>
            </div>
        </div>
        <div v-else>
            <h1 class="text-center fw-bold mt-5" style="color: #645193ff">{{detail}}</h1>
            <div class="d-flex mt-5">
              <div class="row">
                <div class="col-12 col-lg-6">
                  <img :src="findID" class="img-fluid" alt="">
                </div>
                <div class="col-12 col-lg-6 mt-5 mt-lg-0">
                  <h5 class="text-center">{{description}}</h5>
                  <a :href="linkweb"><button class="btn btn-outline-primary mt-5">Go to website</button></a>
                </div>
              </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Detail',
  computed: {
    detail() {
      // extract user from route params
      return this.$route.params.project;
    },
    findID() {
      const image = this.image.filter((item) => item.title === this.$route.params.project);
      return image[0].images;
    },
    findImage() {
      const image = this.image.filter((item) => item.title === this.$route.params.project);
      return image[0].images2;
    },
    description() {
      const image = this.image.filter((item) => item.title === this.$route.params.project);
      return image[0].desc;
    },
    linkweb() {
      const image = this.image.filter((item) => item.title === this.$route.params.project);
      return image[0].linkweb;
    },
  },
  methods: {
    toUppercase() {
      this.gambar = this.image.filter((item) => item.title === this.detail);
      return this.gambar;
    },
  },
  data: () => ({
    profile: 'https://images.unsplash.com/photo-1518791841217-8f162f1e1131?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=800&q=60',
    image: [
      {
        images: '../img/nutziverse.png', images2: 'img/nutziverse.png', title: 'Nutziverse', desc: 'Website untuk menghitung kebutuhan gizi sehari-hari', linkweb: 'https://warungmama.netlify.app/',
      },
      {
        images: '../img/warungmama.png', images2: 'img/nutziverse.png', title: 'WarungMama', desc: 'Website untuk menyediakan kebutuhan sehari-hari', linkweb: 'https://umah-bali.netlify.app/',
      },
      {
        images: '../img/umahbali.png', images2: 'img/nutziverse.png', title: 'UmahBali', desc: 'Website untuk menyediakan informasi properti', linkweb: 'https://nutziverse.netlify.app/',
      },
    ],
    gambar: '',
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
