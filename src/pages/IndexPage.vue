<template>
  <q-page>
    <div class="row flex" style="height: 100%;">
      <div class="col-12" :class="{'q-px-md' : $q.screen.lt.md}">
        <q-card class="col-12 bg_color" style="height: 140px;" :class="{'q-px-md' : $q.screen.lt.md}">
          <q-card-section class="flex flex-center" style="height: 100%;">
            <span class="text-h3">BANNER</span>
          </q-card-section>
        </q-card>
      </div>

      <br />

      <div class="col-12 row q-pa-md">
        <template v-for="product in products" :key="product">
          <ProductCard :product="product" />
        </template>
      </div>
    </div>
  </q-page>
</template>

<script>
import ProductCard from 'src/components/ProductCard.vue'

export default {
  name: 'IndexPage',
  components: { ProductCard },
  data () {
    return {
      products: [
        { name: 'Produto XYZ', description: 'xxxx xxxx xxxx' },
        { name: 'Produto XYZ', description: 'xxxx xxxx xxxx' },
        { name: 'Produto XYZ', description: 'xxxx xxxx xxxx' },
        { name: 'Produto XYZ', description: 'xxxx xxxx xxxx' },
        { name: 'Produto XYZ', description: 'xxxx xxxx xxxx' },
        { name: 'Produto XYZ', description: 'xxxx xxxx xxxx' },
        { name: 'Produto XYZ', description: 'xxxx xxxx xxxx' },
        { name: 'Produto XYZ', description: 'xxxx xxxx xxxx' }
      ]
    }
  }
}
</script>
