<template>
  <div>
      <h3>Customer Reviews</h3>
      <div v-if="reviewer.results">
          <review-card  v-for="review in reviewer.results" :key="review.login.uuid" :review="review"/>
      </div>
  </div>
</template>

<script>
export default {
    data(){
        return{reviewer: []
        }
    },
    async fetch(){
        this.reviewer = await fetch('https://randomuser.me/api/?results=10').then(res =>
            res.json()
        )
    }
}
</script>

<style scoped>

</style>