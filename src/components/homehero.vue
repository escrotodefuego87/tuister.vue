<template>
    <v-container fluid fill-height class="home-hero">
        <v-layout justify-center align-center column pa-5>
            <div class="display-4 font-weight-black light-blue--text text--lighten-3 text-xs-center">The biggest photography community</div>
            <div class="display-3 font-weight-black amber--text darken-1 text-xs-center mb-3">Join us!</div>
            <div class="display-1 font-weight-white white--text text-xs-justify">By Sheryl Sandberg — Chief Operating Officer at Facebook The terrorist attacks in Christchurch were an act of pure evil. All of us at Facebook stand with the victims, their families, the Muslim community, and all of New Zealand. It is deeply tragic when people face violence because of who they are and what they…</div>
            
            <v-btn round large color="primary" to="/login">Iniciar sesion</v-btn>
            <v-btn round large color="amber darken-1 white--text" to="/signup">Registrarse</v-btn>

            
        </v-layout>
    </v-container>
</template>

<script>
export default {
    name: 'HomeHero'
}
</script>

<style scoped>
    .home-hero{
        background: url('https://cdn.pixabay.com/photo/2016/11/19/11/37/automobile-1838782_960_720.jpg');
        background-size: cover;
        width: 100%;
        height: 100%;
    }
</style>
