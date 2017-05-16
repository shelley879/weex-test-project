<template>
  <div class="wrapper">
    <div class="box">
    </div>
  </div>
</template>

<style scoped>
  .wrapper {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-color: #cccccc;
    justify-content: center;
    align-items: center;
  }
  .box {
    width: 200px;
    height: 200px;
    background-color: #fc0000;
  }
</style>

<script>
  module.exports = {
    data: function () {
      return {
        list:[
          ['A', 'B', 'C'],
          ['D', 'E', 'F'],
          ['G', 'H', 'I']
        ]
      }
    }
  }
</script>
