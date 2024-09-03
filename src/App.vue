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
  beforeCreate() {
    // 컴포넌트 생성되기 직전 실행되는 라이프 사이클
    // count 출력 시 undefined 출력
    console.log("beforeCreate", this.count);
  },
  created() {
    console.log("Created!" )
  },
  beforeMount() {
    console.log("beforeMount");
  },
  mounted() {
    // 화면에 실제 컴포넌트 출력 후 실행
    // 코드 작성 순서에 상관 없이 created 실행 후 mounted 출력됨
    console.log("Mounted!")
  },
}
</script>