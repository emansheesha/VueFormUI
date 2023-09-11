<!-- how to deal with props & reference type -->
<template>
  <div v-for="(st, i) in std" :key="i" >
    {{ st }}
  </div>
  <input v-on:click="deleteArr" value="delete" type="submit"/>
  <button @click="updateActive">hire event </button>
 child: {{isActive}}
</template>
<script>
export default {
  props: ["std","isActive"],
  data() {
    return {
      stud: this.std,
    };
  },
  methods:{
    deleteArr(){
        console.log('click')
        return this.stud.pop()
    },
    updateActive(){
      this.$emit('changeActive')
    }
  }
};
</script>
