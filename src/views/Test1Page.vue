<template>
  <VueInstance1 />
</template>

<script lang="ts">
import Vue from 'vue';
import VueInstance1 from '@/components/VueInstance1.vue';

export default Vue.extend({
  components: {
    VueInstance1,
  },

});
</script>
