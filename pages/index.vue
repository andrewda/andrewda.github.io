<template>
  <div :class="`container ${animatingContainer && 'animated fadeIn'}`">
    <div class="content">
      <h1 :class="`title ${animatingTitle && 'animated fadeInDown'}`">
        Hello, I'm <span class="name">Andrew</span>
      </h1>
      <h2 :class="`subtitle ${animatingSubtitle && 'animated fadeIn'}`">
        A Software Engineer 💻 in Corvallis, OR 🏞
      </h2>
      <div :class="`links ${animatingLinks && 'animated fadeIn'}`">
        <nuxt-link to="/experience" class="button--green">
          Experience
        </nuxt-link>
        <a
          href="https://github.com/andrewda"
          target="_blank"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      animatingContainer: true,
      animatingTitle: true,
      animatingSubtitle: true,
      animatingLinks: true,
    }
  },
  mounted() {
    setTimeout(() => this.animatingContainer = false, 1000)
    setTimeout(() => this.animatingTitle = false, 1500)
    setTimeout(() => this.animatingSubtitle = false, 2500)
    setTimeout(() => this.animatingLinks = false, 3500)
  }
}
</script>

<style scoped lang="less">
.container {
  background-repeat: no-repeat;
  background-image: linear-gradient(to right, @black-transparent 200px, @black 650px), url('~assets/single_bw.png');
  background-size: contain;
  background-position: 0 0;
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.content {
  width: calc(100% - 620px);
  position: absolute;
  padding: 20px;
  right: 0;
}

.name {
  color: @green;
}

.links {
  padding-top: 15px;
  animation-delay: 2.5s;
}

@media only screen and (max-width: 1140px) {
  .container {
    background-image: linear-gradient(to bottom, @black 0%, @black-transparent 30%, @black 100%), url('~assets/single_bw.png');
    background-size: cover;
    align-items: flex-end;
  }

  .content {
    width: 100%;
    padding-bottom: 95px;
  }

  .title {
    font-size: 40px;
  }

  .subtitle {
    font-size: 25px;
  }
}
</style>
