<template>
  <div>
    <LikeHeader></LikeHeader>
    <h3>{{totalNumber}}</h3>
    <LikeNumber :total-number="totalNumber"></LikeNumber>
    <LikeNumber :total-number="totalNumber"></LikeNumber>
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
      totalNumber: '8'
    }
  }
}
</script>
