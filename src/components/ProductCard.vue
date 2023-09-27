<template>
  <div class="q-pa-sm" :class="!$q.screen.lt.md ? 'col-12 col-md-3 col-sm-6' : 'col-6'">
    <q-card>
      <img src="https://source.unsplash.com/random" height="250" />

      <q-card-section>
        <div class="text-h5">{{ product.name }}</div>

        <span>{{ product.description }}</span>
      </q-card-section>
    </q-card>
  </div>
</template>

<script>
export default {
  name: 'ProductCard',

  props: {
    product: {
      type: Object,
      required: true
    }
  }
}
</script>
