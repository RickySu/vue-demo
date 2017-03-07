<template>
  <div class="main">
    <com-header></com-header>
    <router-view></router-view>
  </div>
</template>

<script>
import comHeader from './components/_header.vue'
export default {
  components: {
    comHeader
  }
}
</script>

<style src="bootstrap/dist/css/bootstrap.css"></style>
<style src="font-awesome/css/font-awesome.css"></style>
