<!--
 * @Author: your name
 * @Date: 2019-11-11 09:40:10
 -->
<template>
  <div id="app">
    <time-line></time-line>
    <time-line-two></time-line-two>
  </div>
</template>

<script>
import TimeLine from './components/TimeLine'
import TimeLineTwo from './components/TimeLineTwo'
export default {
  name: 'App',
  components: {
    TimeLine,
    TimeLineTwo
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
