<template>
  <div>
    <ul>
      <li v-for="(item,index) in arr" :key="index">
        {{ item }}
        <button @click="del(index)">删除</button>
        </li>
    </ul>
    <button @click="btn">生成</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: [1],
    };
  },
  methods: {
    btn() {
      let randomNum = Math.floor(Math.random() * 99 + 1);
      this.arr.push(randomNum)
    },
    del(index){
      this.arr.splice(index,1)
    }
  },
};
</script>

<style>
</style>