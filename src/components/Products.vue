<template>
    <div>
        <ul>
            <li v-for="product in products">
              <a href="">
              <h2>{{product.title}}</h2>
              <p>{{product.content}}</p>
              </a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
  mounted () {
    this.$http.get('http://demo3913545.mockable.io/products')
    .then((response) => {
      this.products = response.data
    })
  },
  data () {
    return {
      products: []
    }
  }
}
</script>

