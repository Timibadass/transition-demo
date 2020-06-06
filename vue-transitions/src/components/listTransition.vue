<template>
  <div>
    <h1>List/Group Transition</h1>
    <transition-group name="slide-fade" tag="ul">
      <li v-for="user in users" :key="user.id">
        {{user.name}}
        <button @click="removeUser(user.id)">Remove</button>
      </li>
    </transition-group>
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: [
        {
          name: "Vuejs",
          id: 1
        },
        {
          name: "Vuex",
          id: 2
        },
        {
          name: "Router",
          id: 3
        }
      ]
    };
  },
  methods: {
    removeUser(id) {
      let users = this.users.filter(user => user.id !== id);
      this.users = users;
    }
  }
};
</script>

<style>
.slide-fade-enter-active {
  transition: transform 0.3s cubic-bezier(1, 0.5, 0.8, 1),
    color 0.5s cubic-bezier(1, 0.5, 0.8, 1);
}
.slide-fade-leave-active {
  transition: transform 1s cubic-bezier(1, 0.5, 0.8, 1),
    color 1s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter {
  color: mediumblue;
  transform: translateY(20px);
}

.slide-fade-leave-to {
  transform: translateX(100px);
  color: cyan;
}
</style>