<template>
  <div class="container">
    <div class="content">
      <h1 class="title">Experience</h1>

      <div class="job">
        <div class="job-title">
          <span class="box">Systems Engineer</span>
          <span class="box at">@</span>
          <span class="box">OSU Open Source Lab</span>
        </div>
      </div>

      <div class="job">
        <div class="job-title">
          <span class="box">Software Engineering Intern</span>
          <span class="box at">@</span>
          <span class="box">NASA Jet Propulsion Laboratory</span>
        </div>
      </div>

      <div class="job">
        <div class="job-title">
          <span class="box">Software Developer</span>
          <span class="box at">@</span>
          <span class="box">Twenty Ideas</span>
        </div>
      </div>

      <div class="job">
        <div class="job-title">
          <span class="box">Machine Learning Intern</span>
          <span class="box at">@</span>
          <span class="box">Oregon State University</span>
        </div>
      </div>

      <div class="job">
        <div class="job-title">
          <span class="box">Software Lead</span>
          <span class="box at">@</span>
          <span class="box">South Eugene Robotics Team</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
}
</script>

<style scoped>
.container {
  margin: 0 auto;
  padding-top: 50px;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  text-align: center;
}

.content {
  width: 100%;
  padding: 20px;
}

.title {
  margin-bottom: 50px;
}

.job {
  margin-bottom: 20px;
}

.job-title {
  display: flex;
}

.box {
  flex: 1;
  display: flex;
  justify-content: center;
}

.box:first-child {
  justify-content: flex-end;
}

.box:last-child {
  justify-content: flex-start;
}

.at {
  flex: 0 auto;
  padding: 0 20px;
}
</style>