<template>
  <div class="bg-danger">
    <h1>Dynamic Route</h1>
  </div>
</template>

<script>
export default {
  name: 'detail-project',
  computed: {
    detail() {
      // extract user from route params
      return 23;
    },
  },
};
</script>
