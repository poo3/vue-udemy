<template>
  <div>
    <p v-border:solid.round.shadow="{ width: '1px', color: 'red' }">Home</p>
    <h2>{{ title | upperCase }}</h2>
    <p>{{ subTitle | lowerCase }}</p>
  </div>
</template>

<script>
export default {
  directives: {
    border(el, binding) {
      el.style.borderStyle = binding.arg;
      el.style.borderWidth = binding.value.width;
      el.style.borderColor = binding.value.color;
      if (binding.modifiers.round) {
        el.style.borderRadius = "0.5rem";
      }
      if (binding.modifiers.shadow) {
        el.style.boxShadow = "0 2px 5px rgba(0,0,0, 0.26)";
      }
    },
  },
  data() {
    return {
      title: "Welcome to Tokyo",
      subTitle: "Tokyo is great City",
    };
  },
  filters: {
    lowerCase(value) {
      return value.toLowerCase();
    },
  },
};
</script>
