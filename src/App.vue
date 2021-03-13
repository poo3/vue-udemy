<template>
  <div>
    <LikeHeader></LikeHeader>
    <h3>{{totalNumber}}</h3>
    <LikeNumber :totalNumber="totalNumber" @my-click="incrementNumber"></LikeNumber>
    <LikeNumber :totalNumber="totalNumber" @my-click="incrementNumber"></LikeNumber>
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
      totalNumber: 8
    }
  },
  methods: {
    incrementNumber(){
      this.totalNumber += 1;
    }
  }
}
</script>
