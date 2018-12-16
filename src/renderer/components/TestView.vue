<template>
  <v-layout column justify-center>
      <v-flex>
          <img src="/static/meaw.jpg" alt="" class="mb-5">
          <blockquote class="text-xs-center">
              &#8220;{{name.uid}}&#8220;
              <v-btn
              color="warning"
              flat
              router to="/updateTest">Update</v-btn>
          </blockquote>
      </v-flex>
  </v-layout>
</template>

<script>
const axios = require('axios')
export default {
  data: () => ({
    name: ''
  }),
  created () {
    axios.get('http://localhost:5001')
      .then(res => {
        console.log(res)
        this.name = res.data[0]
      })
  }
}
</script>


<style scoped>
    img {
        margin-left: auto;
        margin-right: auto;
        display: block;
        width: 200px;
        height: 200px;
        border-radius: 200px;        
    }
</style>s
