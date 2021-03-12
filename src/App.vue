<template>
  <div>
    <LikeHeader></LikeHeader>
    <h3>{{number}}</h3>
    <LikeNumber :number="number"></LikeNumber>
    <LikeNumber :number="number"></LikeNumber>
  </div>
</template>

<script>
import LikeHeader from './components/LikeHeader.vue'

export default{
  components: {
    LikeHeader
  },
  data(){
    return {
      number: '8'
    }
  }
}
</script>
