<template>
  <div class="hello">
    <h1>{{ standardNum }} + {{ changedNum }} : {{ sumNum }}</h1>
    <h1>{{ standardNum }} - {{ changedNum }} : {{ minorNum }}</h1>
    <h1>{{ standardNum }} * {{ changedNum }} : {{ multiplyNum }}</h1>
    <h1>{{ standardNum }} / {{ changedNum }} : {{ divisionNum }}</h1>
    <b-button
      class="m-1"
      @click="upNum"
    >
      숫자 올리기
    </b-button>
    <b-button
      class="m-1"
      @click="downNum"
    >
      숫자 내리기
    </b-button>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'VueInstance1',
  props: [],
  data() {
    return {
      standardNum: 1,
      changedNum: 1,
    };
  },
  computed: {
    sumNum(): number {
      return this.standardNum + this.changedNum;
    },
    minorNum(): number {
      return this.standardNum - this.changedNum;
    },
    multiplyNum(): number {
      return this.standardNum * this.changedNum;
    },
    divisionNum(): string {
      return (this.standardNum / this.changedNum).toFixed(2);
    },
  },
  watch: {
    changedNum(value, oldValue) {
      console.log('value : ', value);
      console.log('oldValue : ', oldValue);
    },
  },
  methods: {
    upNum() {
      this.changedNum += 1;
    },
    downNum() {
      this.changedNum -= 1;
    },
  },
});
</script>
