<template>
    <v-app>
        <toolbar></toolbar>
        <router-view></router-view>
      

    </v-app>
</template>

<script>

import toolbar from './components/toolbar.vue'
import VeeValidate from 'vee-validate';

export default {

    components:{
        toolbar: toolbar,
 
    }
}
</script>

<style>
    
</style>
