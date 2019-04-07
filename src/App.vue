<template>
    <v-app>
        <toolbar></toolbar>
        <router-view></router-view>
      

    </v-app>
</template>

<script>

import toolbar from './components/toolbar.vue'

export default {

    components:{
        toolbar: toolbar,
 
    }
}
</script>

<style>
    
</style>
