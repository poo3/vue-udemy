<template>
  <div>
    <LikeHeader v-slot="slotProps">
      <h1>{{slotProps.user.firstName}}</h1>
      <h1>トータルのいいね数</h1>
      <h3>{{totalNumber}}</h3>
    </LikeHeader>
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
