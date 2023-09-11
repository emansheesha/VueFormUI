<template>
  <div v-if="user != null">{{ user.name }} is in home component</div>
  <div v-else>{{ name }} is in home component</div>
  <div v-for="(st, i) in students" :key="i">
    {{ st }}
  </div>
  <About :std="students" @changeActive="changeActiveParent" :isActive="isActive"/>
  parent:{{ isActive }}
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
      isActive:false
    };
  },
  methods:{
    changeActiveParent(){
      this.isActive=!this.isActive
    }
  }
};
</script>
