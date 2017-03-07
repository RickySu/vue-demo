<template>
    <div>
        <ul class="product">
            <li v-for="product in products">
              <a href="">
              <h2>{{product.title}} in product</h2>
              <p>{{product.content}}</p>
              </a>
            </li>
        </ul>
    </div>
</template>

<style scoped>
.product h2{
  font-size: 32px;
  color: red;
}
</style>

<style lang="sass?indentedSyntax" type="text/sass" scoped>
.product
  p
    font-size:  24px
    color: black
    display: block
    border: 1px solid
    width: 80%
  li
    list-style: none
</style>

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

