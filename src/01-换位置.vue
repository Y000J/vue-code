<template>
  <div>
    <h1 v-for="(item, index) in arr" :key="index">
      {{ item }}
    </h1>
    <button @click="btn">换位置</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: ["1帅哥", "2美女", "3靓仔"],
    };
  },
  methods: {
    btn() {
      // let temp = this.arr.shift();
      // this.arr.push(temp);
      this.arr.push(this.arr[0])
      this.arr.shift()
    },
  },
};
</script>

<style>
</style>