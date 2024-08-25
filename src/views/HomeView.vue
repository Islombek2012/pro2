<script>
import BaseBtn from '@/components/BaseBtn.vue'
import CardComponent from '../components/CardComponent.vue'
    export default{
      components: {
        CardComponent,
        BaseBtn
      },
      data() {
        return {
          products: [
            {
              id: 1,
              img: 'https://picsum.photos/300/400?random=1',
              title: 'Product 1',
              desc: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugiat quisquam nobis cum deleniti veniam inventore minus quaerat hic voluptatem temporibus!'
            },
            {
              id: 2,
              img: 'https://picsum.photos/300/400?random=2',
              title: 'Product 2',
              desc: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugiat quisquam nobis cum deleniti veniam inventore minus quaerat hic voluptatem temporibus!'
            },
            {
              id: 3,
              img: 'https://picsum.photos/300/400?random=3',
              title: 'Product 3',
              desc: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugiat quisquam nobis cum deleniti veniam inventore minus quaerat hic voluptatem temporibus!'
            },
            {
              id: 4,
              img: 'https://picsum.photos/300/400?random=4',
              title: 'Product 4',
              desc: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugiat quisquam nobis cum deleniti veniam inventore minus quaerat hic voluptatem temporibus!'
            },
            {
              id: 5,
              img: 'https://picsum.photos/300/400?random=5',
              title: 'Product 5',
              desc: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugiat quisquam nobis cum deleniti veniam inventore minus quaerat hic voluptatem temporibus!'
            },
            
          ],
          count: 0 ,
          ozgar: 2,
          user: 'Islombek'
        }
      },
      methods: {
        addCount(par) {
          this.count+=par
        },
        haa(par){
          this.ozgar = 'SALOM salom salomga'
        }
      },
    }
</script>

<template>
  
    <main>
        Home page
        <h1>HomeCount: {{count}}</h1>
        <h1>Click button Component o'zgartiradi: {{ozgar}}</h1>
        <BaseBtn :user="user" @ozgartirish="haa"></BaseBtn>
        <div class="row">
            <CardComponent @qandaydir="addCount" v-for="product, i in products" :key="i" :product="product"></CardComponent>
        </div>
    </main>
    
</template>

<style lang="scss" scoped>
  .row{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  }
</style>
