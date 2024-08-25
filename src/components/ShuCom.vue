<template>
      <div>
            <button @click="change">Clickckckckckckckckckck <br> {{user}}</button>
      </div>
</template>
<script>
export default {
      methods: {
            change() {
                  this.$emit('salom2')
            }
      },
      props: {
            user: {
                  type: String,
                  required: true
            },
      },
}
</script>