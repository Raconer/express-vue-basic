<template>
  <div>
    <h1 id="app"></h1>
  </div>
</template>

<script>
// import Vue from 'vue'
import axios from 'axios'

export default {
  name: 'Test',
  data () {
    let state = {
      getMsg: '',
      postMsg: ''
    };

    return {
      state
    }
  },
  created(){
    console.log(this.state)
    try {
      let urlGet = '/api/getTest';
      axios.get(urlGet, {})
        .then(function (response) {
          console.log("Get Success");
          this.state.getMsg = response.data.msg;
        })
        .catch(function (error) {
          console.log(error);
        });


      let urlPost = '/api/postTest';
      axios.post(urlPost, {name: 'Finiview'}).
        then(function (response) {
          console.log("Post Success");
          this.state.postMsg = response.data.msg;
        })
        .catch(function (error) {
          console.log(error);
        });
        } catch (err) {
          console.log(err);
        }
    }
}
</script>

<style scoped>
</style>