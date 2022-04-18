<template>
  <div class="about">
    <h1>This is an about page</h1>
    <button @click="showAlert">Test</button>
    <div>
      <button @click="addCount">Count</button>
      <div>버튼을 클릭한 횟수 : {{ clickCount }}</div>
    </div>
    <div>{{ aa }}</div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      clickCount: 0
    }
  },
  methods: {
    showAlert () {
      window.alert('테스트')
    },
    addCount () {
      this.clickCount++
    }
  }
}
</script>
