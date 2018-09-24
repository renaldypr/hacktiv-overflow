<template>
  <div class="container">
    <router-link class="text-light" :to="{ name: 'form' }"><button type="button" class="btn btn-primary btn-lg mt-3 mb-3">Ask Question</button></router-link>
    <Card></Card>
  </div>
</template>

<script>
import Card from '@/components/card.vue'

export default {
  components: {
    Card
  }
}
</script>

<style scoped>

</style>
