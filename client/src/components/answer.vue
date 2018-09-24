<template>
  <div>
    <div class="row border-top border-bottom pb-3 pt-3">
      <div class="col-md-1">
        <i class="fas fa-arrow-alt-circle-up"></i>
        <p class="m-0">0</p>
        <i class="fas fa-arrow-alt-circle-down"></i>
      </div>
      <div class="col-md-11 text-left">
        <div id="answerAuthor" class="text-left mb-3 row">
          <div class="col-md-0 ml-3">
            <img id="authorImage" class="rounded-circle" src="https://via.placeholder.com/40x40">
          </div>
          <div class="col-md-3">
            <p class="author mb-0 ">Renaldy</p>
            <p class="text-muted">Answered 24 Sept 2018</p>
          </div>
        </div>
        <p>Question's answer is here.....</p>
        <p>Question's answer is here.....</p>
        <p>Question's answer is here.....</p>
        <p>Question's answer is here.....</p>
        <p>Question's answer is here.....</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.author {
  display: inline-block;
}
#answerAuthor {
  font-size: 14px;
}
</style>
