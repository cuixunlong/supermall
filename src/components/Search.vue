<template>
  <div id="search">
    <input type="text" placeholder="请输入搜索内容">
    <div id="blue"></div>
  </div>
</template>
<script lang="ts">
  import axios from 'axios'

  export default ({
    name: 'Search',
    data() {
      return {}
    },
    mounted() {
      const baseUrl = 'https://www.fastmock.site/mock/f40a92317e832f337e3de5a8d67bd036/api';

      axios.get(`${baseUrl}/test`).then(data => {
        console.log(data)
      })
    },

  })
</script>

<style>
  input {
    width: 90%;
    margin-left: 15px;
    height: 30px;
    border: none;
    background-color: #99999936;
    border-radius: 10px;
    outline: none;
    text-indent: 2em;
  }

  #blue {
    width: 90%;
    height: 100px;
    background-color: #0037ff66;
    margin-left: 15px;
    margin-top: 10px;
    border-radius: 10px;
  }
</style>