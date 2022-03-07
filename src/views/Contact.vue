<template>
    <div class="contact">
        <div class="container">
            <h1 class="fw-bold text-center mt-3" style="color: #645193ff;">Contact me</h1>
            <div class="d-flex flex-column">
                <form action="mailto:muhammadnurudin01@gmail.com" method="post" enctype="text/plain">
                    <input placeholder="Nama" type="text" class="form-control mx-auto my-2 w-75" id="exampleFormControlInput1" v-model="nama" >
                    <input placeholder="Email" type="email" class="form-control mx-auto my-2 w-75" id="exampleFormControlInput1" v-model="email" >
                    <textarea placeholder="Pesan" class="form-control my-2 w-75 mx-auto" id="exampleFormControlTextarea1" rows="3" v-model="pesan"></textarea>
                    <input type="Submit" value="Send" class="btn btn-primary" style="background-color: #645193ff;">
                </form>
            </div>
        </div>
    </div>

</template>

<script>
export default {
  data() {
    return {
      nama: '',
      email: '',
      pesan: '',
    };
  },
};
</script>
