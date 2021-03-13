<template>
  <div>
    <LikeHeader></LikeHeader>
    <h3>{{totalNumber}}</h3>
    <LikeNumber :totalNumber="totalNumber"></LikeNumber>
    <LikeNumber :totalNumber="totalNumber"></LikeNumber>
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
