<!--suppress HtmlUnknownTarget -->
<template lang="pug">
  .home
    img(src='../assets/logo.png')
    HelloWorld(msg='Welcome to Your Vue.js App')
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

@Component({
  components: {
    HelloWorld,
  },
})
export default class Home extends Vue {}
</script>
