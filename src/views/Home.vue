<template lang="pug">
  hello-world
</template>

<script lang="ts">
  import Vue from 'vue'
  import HelloWorld from '../components/LifeBit.vue'

  export default Vue.extend({
    name: 'Home',

    components: {
      HelloWorld,
    },
  })
</script>
