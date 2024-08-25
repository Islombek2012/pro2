<template>
      <div  class="btn">
            Click button Component
            <hr>
            <ShuCom :user="user" @salom2="ozgartirvor"></ShuCom>
      </div>
</template>

<script>
import ShuCom from './ShuCom.vue'
      export default {
          components: {
            ShuCom,
          },
           methods: {
            ozgartirvor() {
                  this.$emit('ozgartirish')
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

<style lang="scss">
      .btn{
            padding: 15px 25px;
            background-color: lime;   
            display: inline-block;     
            color: #fff;
            font-size: 22px;
            border-radius: 10px;   
            margin: 30px;
            cursor: pointer;
      }
</style>