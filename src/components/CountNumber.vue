<template>
  <div>
    <LikeNumber :totalNumber="totalNumber" @my-click="incrementNumber"></LikeNumber>
  </div>
</template>

<script>
import {countNumber} from "@/CountNumber";

export default{
  mixins: [countNumber],
  
}
</script>
