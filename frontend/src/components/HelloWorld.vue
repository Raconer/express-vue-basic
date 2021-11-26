<template>
  <div>
    <h1>{{state.getMsg}}</h1>
    <h1>{{state.postMsg}}</h1>
  </div>
</template>

<script>
import { onMounted, reactive }from 'vue'
import axios from 'axios'

alert("start");

export default {
  name: 'Test',
  setup () {
    const state = reactive ({
      getMsg: '',
      postMsg: ''
    })

    onMounted(() => {
      try {
        let urlGet = '/api/getTest';
        axios.get(urlGet, {
        })
            .then(function (response) {
              alert("Get Success");
              state.getMsg = response.data.msg
            })
            .catch(function (error) {
              alert(error);
            });


        let urlPost = '/api/postTest';
        axios.post(urlPost, {
          name: 'Finiview'
        }).then(function (response) {
          alert("Post Success");
          state.postMsg = response.data.msg
        })
            .catch(function (error) {
              alert(error);
            });
      } catch (err) {
        console.log(err);
      }
    });

    return {
      state
    }
  }
}
</script>

<style scoped>
</style>