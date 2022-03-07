<template>
    <div class="container bg-danger">
        <h1>Test</h1>
        <detail-project></detail-project>
    </div>
</template>

<script>
import DetailProject from '../components/DetailProject.vue';

export default {
  name: 'Project',
  components: {
    DetailProject,
  },
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
