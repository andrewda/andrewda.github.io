<template>
  <div>
    <div class="menu animated fadeIn">
      <nuxt-link to="/">Home</nuxt-link>
      <nuxt-link to="/experience">Experience</nuxt-link>
      <nuxt-link to="/projects">Projects</nuxt-link>
      <nuxt-link to="/contact">Contact</nuxt-link>
    </div>
    <nuxt />
  </div>
</template>

<script>
export default {
  mounted() {
    console.log(this.$nuxt.$route.name)
  }
}
</script>

<style scoped>
.menu {
  position: absolute;
  z-index: 100;
  right: 0;
  top: 0;
  padding: 20px;
  animation-duration: .5s;
}

.menu > * {
  padding: 5px;
  font-size: 20px;
  font-weight: 500;
  text-decoration: none;
  color: #526488;
  border: solid transparent 1px;
  border-radius: 5px;
}

.nuxt-link-exact-active {
  border: solid whitesmoke 1px;
}
</style>

<style>
html {
  font-family: 'Montserrat', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  background-color: rgb(12, 12, 12);
  color: #dff9fb;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}

.title {
  font-family: 'Montserrat', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 70px;
  color: #526488;
  letter-spacing: 1px;
  animation-delay: 0.5s;
}

.subtitle {
  font-family: 'Montserrat', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-weight: 300;
  font-size: 35px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
  animation-delay: 1.5s;
}
</style>
