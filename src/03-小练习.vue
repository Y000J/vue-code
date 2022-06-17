<template>
  <div>
    <input type="text" v-model="ipt" />
    <button @click="btn">确定</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      ipt: "aabbbbsaa",
    };
  },
  methods: {
    btn() {
      let arr =[]
      let arr1=[]
      for (let i = 0; i < this.ipt.length; i++) {
        const ele = this.ipt[i];
        arr1.push(ele)
        if(arr1.slice(arr1.indexOf(ele)).every((item)=>{
          return item===ele
        })){
          arr.push(ele)
        } 
      }
      console.log(arr.join());
    },
  },
};
</script>

<style>
</style>