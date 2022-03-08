<template>
  <Button msg="ボタンを押してね。" @push="push()" />
</template>

<script>
import Button from './components/Button.vue'

export default {
  name: 'App',
  components: {
    Button
  },
  setup() {
    const push = () => {
      const audio = new Audio(require('@/assets/intercom.mp3'))
      audio.play();
    }

    return {
      push
    }
  }
}
</script>

<style>
body {
  margin: 0;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
