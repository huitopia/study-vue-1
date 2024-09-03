<template>
  <h1
      v-once
      @click="add">{{ msg }}</h1>
  <h1 v-html="msg"></h1>
</template>

<script>
  export default {
    data(){
      return{
        msg: "<div style='color: blue'>Hello!!</div>"
      }
    },
    methods:{
      add(){
        this.msg += "!"
      }
    }
  }
</script>