<template>
  <div class="wrapper" @click="update">
    <image :src="logoUrl" class="logo"></image>
    <text class="title">Hello {{target}}</text>
    <div class="box" @click="onclick" @longpress="onlongpress" @appear="onappear"  @disappear="ondisappear"></div>
  </div>
</template>

<style>
  .wrapper { align-items: center; margin-top: 120px; }
  .title { font-size: 48px; }
  .logo { width: 360px; height: 82px; }
  .box {
    border-width: 2px;
    border-style: solid;
    border-color: #BBB;
    width: 250px;
    height: 250px;
    margin-top: 250px;
    margin-left: 250px;
    background-color: #EEE;
  }
</style>

<script>
  const modal = weex.requireModule('modal')

  export default {
    data: {
      logoUrl: 'https://alibaba.github.io/weex/img/weex_logo_blue@3x.png',
      target: 'World'
    },
    methods: {
      update: function (e) {
        this.target = 'Weex'
        console.log('target:', this.target)
      },
      onclick (event) {
        console.log('onclick:', event)
        modal.toast({
          message: 'onclick',
          duration: 0.8
        })
      },
      onlongpress (event) {
        console.log('onlongpress:', event)
        modal.toast({
          message: 'onlongpress',
          duration: 0.8
        })
      },
      onappear (event) {
        console.log('onappear:', event)
        modal.toast({
          message: 'onappear',
          duration: 0.8
        })
      },
      ondisappear (event) {
        console.log('ondisappear:', event)
        modal.toast({
          message: 'ondisappear',
          duration: 0.8
        })
      }
    }
  }
</script>
