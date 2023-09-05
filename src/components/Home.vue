<template>

    <div v-if="user !=null">{{ user.name }} is in home component</div>
    <div v-else>{{ name }} is in home component</div>
</template>
<script>
export default {
    data(){
        return {
            name:'moustafa',
            user:JSON.parse(localStorage.getItem('user'))
        }
    }
}
</script>