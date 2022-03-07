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
                <router-link class="btn btn-outline-success" :to="{name: 'Project', params: {project: items.title}}">Detail</router-link>
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
      { images: 'https://media.istockphoto.com/photos/snowcapped-k2-peak-picture-id1288385045?b=1&k=20&m=1288385045&s=170667a&w=0&h=3M3ZRl1bxOGxcvmYZ-TOtuJ3idm0psm4c7GFba1TA5g=', title: 'Gunung Sumatra', desc: 'ini adalah gunung Sumatra' },
      { images: 'https://media.istockphoto.com/photos/snowy-peaks-of-the-caucasus-mountains-picture-id1327243304?b=1&k=20&m=1327243304&s=170667a&w=0&h=eVHzfEbMv7ki-LY0p-KO4L7X19KaqMYe2GmfPwcrGjU=', title: 'Gunung Jawa', desc: 'ini adalah gunung Jawa' },
      { images: 'https://media.istockphoto.com/photos/moose-at-maroon-lake-a-young-moose-with-only-one-antler-walking-and-picture-id1288537145?b=1&k=20&m=1288537145&s=170667a&w=0&h=DP5AU3_JBwGiCDJellQR6NMmrycDsrjd89yccPlVgJc=', title: 'Gunung Kalimantan', desc: 'ini adalah gunung Kalimantan' },
    ],
  }),
};
</script>
