<template>
  <h1>{{count}}</h1>
</template>
<script>
export default {
  data(){
    return{
      count:2
    }
  },
  mounted() {
    // 화면에 실제 컴포넌트 출력 후 실행
    // 코드 작성 순서에 상관 없이 created 실행 후 mounted 출력됨
    console.log("Mounted!")
  },
  created() {
    console.log("Created!")
  },
}
</script>