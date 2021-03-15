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
    <EventTitle v-model="eventData.title"></EventTitle>
    <CountNumber></CountNumber>
  </div>
</template>

<script>
import CountNumber from './components/CountNumber'
import LikeHeader from './components/LikeHeader.vue'
import About from './components/About'
import Home from './components/Home'
import EventTitle from './components/EventTitle'
import { countNumber } from "@/CountNumber"

export default{
  mixins: [countNumber],
  components: {
    LikeHeader,
    About,
    Home,
    EventTitle,
    CountNumber
  },
  data(){
    return {
      currentComponent: 'Home',
      eventData: {
        title: 'タイトル'
      }
    }
  }
}
</script>
