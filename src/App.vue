<template>
  <div id="app">
   <router-link to="/index">Go to index</router-link>
    <router-link to="/table">Go to table</router-link>
      <router-view></router-view>
  </div>
</template>
<script>
export default {
  data () {
    return {
      msg: 'Use Vue 2.0 Today!'
    }
  },

  methods: {
    startHacking () {
      this.$notify({
        title: 'It Works',
        message: 'We have laid the groundwork for you. Now it\'s your time to build something epic!',
        duration: 6000
      })
    }
  }
}
</script>
