<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <b-button variant="success">Button</b-button>
    <b-alert show variant="danger">Danger Alert</b-alert>
  </div>
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
