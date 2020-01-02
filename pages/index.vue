<template>
  <div class="container animated fadeIn">
    <div class="content">
      <h1 class="title animated fadeInDown">
        Hello, I'm <span class="name">Andrew</span>
      </h1>
      <h2 class="subtitle animated fadeIn">
        Software Engineer 💻 in Corvallis, OR 🏞
      </h2>
      <div class="links animated fadeIn">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green"
        >
          Experience
        </a>
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

<style>
html {
  background-color: black;
}

.container {
  background-repeat: no-repeat;
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0) 200px,rgb(0, 0, 0, 1) 650px), url('~assets/single_bw.png');
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

.name {
  color: #3b8070;
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

.links {
  padding-top: 15px;
  animation-delay: 2.5s;
}

@media only screen and (max-width: 1140px) {
  .container {
    background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0) 0%, rgb(0, 0, 0, 0.9) 100%), url('~assets/single_bw.png');
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
