<template>
  <div>
     <router-link class="btn btn-default" :to="{name: 'Home'}">Home</router-link>
     <router-link class="btn btn-default" :to="{name: 'Products'}">Products</router-link>
     <a class="btn btn-default" href="#" @click="activeTab='message'">Messages</a>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      activeTab: 'home'
    }
  }
}
</script>
