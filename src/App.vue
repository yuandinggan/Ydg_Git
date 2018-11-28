<template>
  <div id="app">
      <header :class="{red:isred}">
          <div v-html="msg"></div>
      </header>
      <button @click="Btn()">按钮</button>
      <div v-if="true">
        我是if 的 true
      </div>
      <form action="">
        <input type="text" name="" id="" v-model="text">
        <input type="checkbox" value="1" v-model="checkboxList">
        <label for="">1</label>
        <input type="checkbox" value="2" v-model="checkboxList">
        <label for="">2</label>
        <input type="checkbox" value="3" v-model="checkboxList">
        <label for="">3</label>
      </form>
      <div>{{text}}</div>
      <div>checkboxList的值:{{checkboxList}}</div>

      <h1>我是一台什么会啊 </h1>
      <span>不知道什么啊</span> 
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      msg: this.shouList(),
      isred:true,
      text:"",
      checkboxList:[]
    };
  },
  methods: {
    shouList(){
      let str="";
      for(var i=0;i<6;i++){
        str+="<h1><span></span></h1>";
      }
      return str;
    },
    Btn(){
      this.isred=!(this.isred)
    }
  }
};
</script>

<style>
header {
  width: 100vw;
  height: 85px;
  background-color: green;
}
.red{
  background-color: steelblue;
}
</style>
