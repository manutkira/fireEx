<template>
<div>
  <div class="container">
      <large-card
        v-for="cardInfo in largeCardInfo.slice(0,1)"
        :key="cardInfo.id" 
        :cardsSection="cardInfo"/>
        <small-card v-for="cardInfo in smallCardInfo" :key="cardInfo.id" :cardsSection="cardInfo"/>
  </div>
</div>
</template>

<script>
import LargeCard from '~/components/LargeCard.vue'
import {largeCardSections, smallCardSections} from '@/assets/data'
import SmallCard from '~/components/SmallCard.vue'
import Navbar from '~/components/Navbar.vue'
export default {
  components: { LargeCard, SmallCard,
    Navbar },
    data(){
        return{
            largeCardInfo: largeCardSections,
            smallCardInfo: smallCardSections,
        }
    }
}
</script>

<style>

</style>