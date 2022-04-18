<template>
  <div class="hello">
    <div>{{ AAAA }}</div>
    <!-- <div>테스트 변수</div> -->
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
    </p>
    <h3>Installed CLI Plugins</h3>
    <button @click="bbb">버튼</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
    return {
      gift: '선물'
    }
  },
  props: {
    // 부모의 데이터를 받을 때 사용하는 
    AAAA: {
      type: String,
      required: false
    }
  },
  methods: {
    bbb () {
      console.log('선물 보냄')
      this.$emit('toYou', this.gift)
      // 부모한테 선물을 보내고 싶어!!!
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
