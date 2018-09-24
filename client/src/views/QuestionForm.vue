<template>
  <div>
    <h1 class="text-light">Post a New Article</h1>
    <p class="mt-4 text-light" v-if="!nowlogin">Please <a class="text-light" href="#" data-toggle="modal" data-target="#loginModal">login</a> to post an article</p>
    <div v-else class="card mt-4 ml-5 mr-5 mb-4">
      <div class="card-body">
        <div class="form-group">
          <input id="title" type="text" class="form-control" placeholder="Article Title" required="required" v-model="titleInput">
        </div>
        <div class="form-group">
          <textarea v-model="contentInput" class="form-control" rows="6" id="content" placeholder="Write your content"></textarea>
        </div>
        <div class="form-group">
          <button type="button" class="btn btn-secondary btn-block" v-on:click="submitArticle()">Post Article</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nowlogin: true,
      titleInput: '',
      contentInput: ''
    }
  },
  methods: {
    submitArticle: function () {

    }
  }
}
</script>

<style>

</style>
