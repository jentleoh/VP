<template>
<div id="container">
{{count}}
<b-button variant="success" @click="increase">올리기</b-button>
<b-button variant="danger" @click="decrease">내리기</b-button>
</div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({})
export default class Counter extends Vue {
    count=0

    increase():void {
        console.log('increase', this.count);
        this.count += 1;
    }
    decrease():void {
        console.log('decrease', this.count);
        this.count -= 1;
    }
}
</script>

<style scoped>
#container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>