<template>
  <div class="home">
    <div class="box">{{ msg }}</div>
    <div class="box1">
      <span v-for="(item, index) in arr1" :key="index">{{ item }}</span>
    </div>
    <button @click="btn">开始</button>
    <input type="text" placeholder="请输入" v-model="iptvalue" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      msg: "你好世界hello world",
      arr: [5, 48, 94, 12, 10],
      arr1: [],
      iptvalue: ""
    };
  },
  methods: {
    btn() {
      this.arr1 = this.arr.filter(v => v >= 18);
      console.log(this.iptvalue);
    }
  },
  mounted() {
    // this.$axios.get("/static/mock.json", {}).then(res => {
    //   console.log(res);
    // });
  }
};
</script>
<style lang="less" scoped>
.home {
  font-size: 62.5%;
}
.box {
  font-size: 2em;
}
</style>
