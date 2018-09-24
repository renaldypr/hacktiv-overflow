<template>
  <div class="card mb-3">
        <div class="card-body pb-0">
            <div class="row">
                <div class="col-md-1">
                  <p>0</p>
                  <p>Votes</p>
                </div>
                <div class="col-md-1">
                  <p>0</p>
                  <p>Answers</p>
                </div>
                <div class="col-md-10">
                  <h4><router-link :to="{ name: 'details', params: { id: 'abcd1234' } }">This is my question?</router-link></h4>
                  <p>Renaldy | 26 Sept 2018 </p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>

</style>
