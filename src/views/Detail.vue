<template>
    <div class="container">
        <div v-if="detail === undefined">
            <div class="row mt-5">
            <div v-for="(items, index) in image" :key="index" class="col-4">
                <div class="card">
                <img :src="items.images" class="card-img-top" alt="...">
                <div class="card-body">
                    <h5 class="card-title">{{items.title}}</h5>
                    <p class="card-text">{{items.desc}}</p>
                    <router-link class="btn" :to="{name: 'Project', params: {project: items.title}}">Detail</router-link>
                </div>
                </div>
            </div>
            </div>
        </div>
        <div v-else>
            <h1 class="text-center text-black">{{detail}}</h1>
            <div class="d-flex justify-content-around mt-5">
            <img :src="findID" alt="">
            <h3 class="text-start">{{description}}</h3>
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
    description() {
      const image = this.image.filter((item) => item.title === this.$route.params.project);
      return image[0].desc;
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
      { images: 'https://media.istockphoto.com/photos/snowcapped-k2-peak-picture-id1288385045?b=1&k=20&m=1288385045&s=170667a&w=0&h=3M3ZRl1bxOGxcvmYZ-TOtuJ3idm0psm4c7GFba1TA5g=', title: 'Gunung Sumatra', desc: 'ini adalah gunung Sumatra' },
      { images: 'https://media.istockphoto.com/photos/snowy-peaks-of-the-caucasus-mountains-picture-id1327243304?b=1&k=20&m=1327243304&s=170667a&w=0&h=eVHzfEbMv7ki-LY0p-KO4L7X19KaqMYe2GmfPwcrGjU=', title: 'Gunung Jawa', desc: 'ini adalah gunung Jawa' },
      { images: 'https://media.istockphoto.com/photos/moose-at-maroon-lake-a-young-moose-with-only-one-antler-walking-and-picture-id1288537145?b=1&k=20&m=1288537145&s=170667a&w=0&h=DP5AU3_JBwGiCDJellQR6NMmrycDsrjd89yccPlVgJc=', title: 'Gunung Kalimantan', desc: 'ini adalah gunung Kalimantan' },
    ],
    gambar: '',
  }),
};
</script>
