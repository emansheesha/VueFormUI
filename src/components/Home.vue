<template>
  <div v-if="user != null">{{ user.name }} is in home component</div>
  <div v-else>{{ name }} is in home component</div>
  <div v-for="(st, i) in students" :key="i">
    {{ st }}
  </div>
  <About :std="students"/>
</template>
<script>
import About from "./About.vue";
export default {
  components: {
    About,
  },
  data() {
    return {
      name: "moustafa",
      user: JSON.parse(localStorage.getItem("user")),
      students: ["eman", "ali", "ahmed"],
    };
  },
};
</script>
