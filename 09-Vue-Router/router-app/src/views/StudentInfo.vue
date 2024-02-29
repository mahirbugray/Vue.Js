<template>
  <div>
    <h3>Öğrenci Bilgi Sayfası</h3>
    <!-- <p>Öğrenci ID: {{$route.params.id}}</p> -->
    <p>Öğrenci ID: {{id}}</p>
  </div>
</template>

<script>
export default {
  props:['id']
  // data() {
  //   return {
  //     studentID: this.$route.params.id
  //   }
  // },     burada tanımlayıp studentID yi içeri vererek de çağırabiliriz.
}
</script>

<style>

</style>