<template>
  <div id="form">
    <h1 class="text-dark mt-4">Post a New Question</h1>
    <p class="mt-4 text-dark" v-if="!isLogin">Please <a class="text-dark" href="#" data-toggle="modal" data-target="#loginModal">login</a> to post an article</p>
    <div v-else class="card mt-4 mb-4 w-75 mx-auto">
      <div class="card-body">
        <div class="form-group">
          <input id="title" type="text" class="form-control" placeholder="Question Title" required="required" v-model="titleInput">
        </div>
        <div class="form-group">
          <textarea v-model="contentInput" class="form-control" rows="6" id="content" placeholder="Write your question"></textarea>
        </div>
        <div class="form-group">
          <button type="button" class="btn btn-secondary btn-block" v-on:click="submitQuestion()">Post Question</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

let url = 'http://localhost:3000'

export default {
  data() {
    return {
      titleInput: '',
      contentInput: ''
    }
  },
  methods: {
    submitQuestion: function () {
      axios({
        method: 'post',
        url: `${url}/questions`,
        headers: {
          token: localStorage.getItem('token')
        },
        data: {
          title: this.titleInput,
          content: this.contentInput
        }
      })
        .then(result => {    
          this.$router.push('/questions')
        })
        .catch(err => {
          console.log(err.response.data.message)
        })
    }
  },
  computed: {
    isLogin() {
      return this.$store.state.isLogin
    }
  }
}
</script>

<style scoped>
#form {
  height: auto;
  min-height: 100vh;
}
</style>
