<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld 
      :AAAA="test"
      @toYou="forMe"
    >
    </HelloWorld>
    <!-- <ul>
      <li v-for="i in list" :key="i">{{ i  }}</li>
    </ul> -->
    <!-- 데이터를 넘길때는 v-bind 라는 것을 이용한다 :'받을 이름':'보낼 것' -->
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  data () { 
    return {
      test: '테스트 변수',
      array: ['1', '2', '3'],
      list: ['소갈비', '감자', '당근', '무', '깐 밤', '소갈비찜 양념', '밥']
    }
  },
  components: {
    HelloWorld
  },
  methods: {
    forMe (aa) {
      console.log(aa + ' 받음')
    }
  }
}
</script>
