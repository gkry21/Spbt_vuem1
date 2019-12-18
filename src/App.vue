<template>
<div id="app"> <!-- 메인에서 id를 인식해서 실행된다. -->
  <child-form :headerText="header" :footerText="footer"> // 템플릿에서는 소문자로 만들어야한다. 대문자 생성시 뻗을 수 있다.
   <p>{{message}}</p>
  </child-form>
</div>
</template>
<script>
import ChildForm from "@/components/Child.vue"
export default{
  name: "app",
  components: {ChildForm}, // 파스칼로 생성!
  data(){
    return {
      header: "슬롯 헤드 테스트",
      footer: "슬롯 푸터 테스트",
      message: "APP의 컨텐츠"
    }
  }
}
</script>
<style scoped></style>