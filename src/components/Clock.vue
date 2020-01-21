<template>
  <div id="Clock">{{ time }}</div>
</template>

<script>
export default {
  name: 'Clock',
  data: function() {
    return { time: 'time' };
  },
  mounted: function showTime() {
    window.setInterval(() => {
      var date = new Date();
      var h = date.getHours();
      var m = date.getMinutes();
      var s = date.getSeconds();
      var session = 'AM';

      if (h == 0) {
        h = 12;
      }

      if (h > 12) {
        h = h - 12;
        session = 'PM';
      }

      h = h < 10 ? '0' + h : h;
      m = m < 10 ? '0' + m : m;
      s = s < 10 ? '0' + s : s;

      this.time = h + ':' + m + ':' + s + ' ' + session;
    }, 1000);
  }
};
</script>

<style scoped>
#Clock {
  color: #17d4fe;
  font-size: 60px;
  font-family: Orbitron;
  letter-spacing: 7px;
}
</style>
