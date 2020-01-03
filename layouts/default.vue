<template>
  <div v-touch:swipe="swipeHandler">
    <div class="menu animated fadeIn">
      <nuxt-link v-for="p in pages" :key="p.path" :to="p.path">{{ p.name }}</nuxt-link>
    </div>
    <nuxt />
  </div>
</template>

<script>
const pages = [
  { name: 'Home', path: '/' },
  { name: 'Experience', path: '/experience' },
  { name: 'Projects', path: '/projects' },
  { name: 'Contact', path: '/contact' }
]

export default {
  data() {
    return {
      pages
    }
  },
  methods: {
    swipeHandler(direction) {
      if (direction !== 'left' && direction !== 'right') return

      let index = pages.map(p => p.path).indexOf(this.$nuxt.$route.path) + (direction === 'left' ? 1 : -1)

      if (index < 0) index = 0
      else if (index >= pages.length) index = pages.length - 1

      this.$router.push(pages[index].path)
    }
  }
}
</script>

<style scoped lang="less">
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
  color: @green;
  border: solid transparent 1px;
  border-radius: 5px;

  @media @mobile {
    font-size: 12px;
  }
}

.nuxt-link-exact-active {
  border: solid @white 1px;
}
</style>