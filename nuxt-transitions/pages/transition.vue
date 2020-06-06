<template>
  <div>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Labore libero
      odio, asperiores debitis harum ipsa neque cum nulla incidunt explicabo ut
      eaque placeat qui, quis voluptas. Aut necessitatibus aliquam veritatis.
    </p>
    <nuxt-link to="/">home</nuxt-link>
  </div>
</template>

<script>
export default {
  transition: {
    name: "fade",
    mode: "out-in"
  },
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
