<template>
  <div class="container">
    <h3 class="text-left mt-4">This is my question?</h3>
    <div class="row border-top pb-3 pt-3">
      <div class="col-md-1">
        <i class="fas fa-arrow-alt-circle-up"></i>
        <p class="m-0">0</p>
        <i class="fas fa-arrow-alt-circle-down"></i>
      </div>
      <div class="col-md-11 text-left">
        <p>Question description is here.....</p>
        <p>Question description is here.....</p>
        <p>Question description is here.....</p>
        <p>Question description is here.....</p>
        <p>Question description is here.....</p>
        <div class="text-right mb-3">
          <p class="mb-0">Asked by:</p>
          <img id="authorImage" class="rounded-circle mr-2" src="https://via.placeholder.com/40x40">
          <p class="author ml-2">Renaldy  |  24 Sept 2018</p>
        </div>
      </div>
    </div>
    <h4 class="text-left">4 Answers</h4>
    <Answer></Answer>
  </div>
</template>

<script>
import Answer from '@/components/answer.vue'

export default {
  props: [ 'id' ],
  components: {
    Answer
  },
  data() {
    return {
      
    }
  }
}
</script>

<style scoped>
.author {
  display: inline-block;
}
</style>
