<template>
  <div>
    <transition name="fade" appear mode="out-in">
      <p v-if="show" key="visible">Now you see me!</p>
      <p v-else key="notVisible">Now you don't!</p>
    </transition>
    <button @click="show = !show">click me</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: true
    };
  }
};
</script>

<style>
p {
  color: green;
}
.fade-enter-active {
  transition: transform 0.3s cubic-bezier(1, 0.5, 0.8, 1),
    color 0.5s cubic-bezier(1, 0.5, 0.8, 1);
}
.fade-leave-active {
  transition: transform 1s cubic-bezier(1, 0.5, 0.8, 1),
    color 1s cubic-bezier(1, 0.5, 0.8, 1);
}

.fade-enter {
  color: mediumblue;
  transform: translateY(20px);
}

.fade-leave-to {
  transform: translateX(100px);
  color: cyan;
}
</style>