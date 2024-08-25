<template>
      <div class="card">
            <img :src="product.img" :alt="product.id">
            <h1>{{product.title}}</h1>
            <p>{{product.desc}}</p>
            <div>Count: {{count}}</div>
            <button @click="plus(3)">Click me...</button>
      </div>
</template>
<script>
export default {
      data() {
            return {
                  count: 0
            }
      },
      methods: {
            plus(par) {
                  this.$emit('qandaydir', par)
            }
      },
      props: {
      product: {
            type: Object,
            default: true,
            required: true,
      },
  },
}
</script>