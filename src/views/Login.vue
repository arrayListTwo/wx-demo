<template>
  <div class="Login">
    Login
  </div>
</template>

<script>
export default {
  name: 'Login',
  created () {
    console.log(window.location.href)
    console.log(this.getQueryString(window.location.href, 'code'))
  },
  methods: {
    getQueryString (urlStr, name) {
      const url = new URL(urlStr)
      return url.searchParams.get(name)
    }
  }
}
</script>

<style lang="stylus" scoped>

</style>
