<template>
  <div class="container">
    <my-item
      v-for="item in myRental"
      :key="item.id"
      :item="item" />
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  layout: 'no-navpage',
  computed: {
    ...mapState(['myRental'])
  }
  }
</script>

<style>

</style>