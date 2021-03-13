<template>
  <div>
    <slot name="title" :user="user"></slot>
    <slot name="number">
      デフォルトのいいね数が入ります
    </slot>
  </div>
</template>

<script>
export default{
  data(){
    return {
      user: {
        firstName: "Jack",
        lastName: "Smith"
      }
    }
  },
}
</script>
