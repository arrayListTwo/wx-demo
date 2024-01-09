<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <van-button @click="wxAuthorize">微信授权</van-button>
  </div>
</template>

<script>

export default {
  name: 'HomeView',
  methods: {
    wxAuthorize () {
      const redirectUri = window.encodeURIComponent('http://6f857685.r3.cpolar.cn/#/login')
      window.location = `https://open.weixin.qq.com/connect/oauth2/authorize?appid=wx3ec10050b126c608&redirect_uri=${redirectUri}&response_type=code&scope=snsapi_userinfo&state=STATE#wechat_redirect`
    }
  }
}
</script>
