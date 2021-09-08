<template lang="pug">
  v-app
    v-app-bar(app color='#6441a5' dark)
      .d-flex.align-center
        v-img.shrink.mt-1(alt='LifeBit Logo' contain src='https://gitlab.com/uploads/-/system/project/avatar/10635262/lifebit.png' transition='scale-transition' width='70')
          v-img.shrink.mt-1.hidden-sm-and-down(alt='LifeBit Name' contain min-width='70' src='https://gitlab.com/uploads/-/system/project/avatar/10635262/lifebit.png' width='70').
      v-app-bar-title
        router-link(to="/" style="cursor: pointer" tag="span")
          | {{ appTitle }}
      v-spacer
      v-app-bar-items(class="hidden-xs-only")
      v-btn(flat v-for='item in menuItems' :key='item.title' :to='item.path')
        v-icon(left color='#cccccc') {{ item.icon }}
        | {{ item.title }}

    v-main
      router-view

</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'App',
  data(){
    return {
      appTitle: 'LifeBit',
      sidebar: false,
      menuItems: [
        { title: 'Home', path: '/home', icon: 'fa-home'},
        { title: 'Help', path: '/help', icon: 'fa-question-circle'},
        { title: 'About', path: '/about', icon: 'fa-info-circle'}
      ]
    }
  },
});
</script>

<style lang="sass">
  

</style>
