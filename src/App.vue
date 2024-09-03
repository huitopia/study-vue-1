<template>
  <h1
      v-once
      @click="add">{{ msg }}</h1>
</template>

<script>
  export default {
    data(){
      return{
        msg: "hello world!"
      }
    },
    methods:{
      add(){
        this.msg += "!"
      }
    }
  }
</script>