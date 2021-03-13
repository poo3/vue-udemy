<template>
  <div>
    <LikeHeader #default="slotProps">
      <h1>{{slotProps.user.firstName}}</h1>
      <h1>トータルのいいね数</h1>
      <h3>{{totalNumber}}</h3>
    </LikeHeader>
    <LikeNumber :totalNumber="totalNumber" @my-click="incrementNumber"></LikeNumber>
    <button @click="currentComponent = 'Home' ">Home</button>
    <button @click="currentComponent = 'About'">About</button>
    <component :is="currentComponent"></component>
  </div>
</template>

<script>
import LikeHeader from './components/LikeHeader.vue'
import About from './components/About'
import Home from './components/Home'

export default{
  components: {
    LikeHeader,
    About,
    Home
  },
  data(){
    return {
      totalNumber: 8,
      currentComponent: 'Home'
    }
  },
  methods: {
    incrementNumber(){
      this.totalNumber += 1;
    }
  }
}
</script>
