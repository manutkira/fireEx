<template>
<div>
  <div class="container">
  <hero/>
  <large-card
    v-for="cardInfo in largeCardInfo"
    :key="cardInfo.id"
    :cardsSection="cardInfo">
    </large-card>
  <small-card
    v-for="cardInfo in smallcardInfo"
    :key="cardInfo.id" 
    :cardsSection="cardInfo"/>
  </div>
</div>
</template>

<script>
import {largeCardSections, smallCardSections} from '@/assets/data'
import Navbar from '~/components/Navbar.vue'
export default {
  components: { Navbar },
  data(){
    return{
      largeCardInfo: largeCardSections,
      smallcardInfo: smallCardSections,
    }
  }
}
</script>