<template>
    <div>
        <v-container grid-list-xl fluid fill-height>
            <v-layout row wrap>
                <v-card id="formBody">
                    <v-flex xs10 offset-xs1>
                        <v-form>
                            <h1>Iniciar sesion en Tuister</h1>

                            <v-text-field label="Nickname" required>
                            </v-text-field>

                            <v-text-field type="password" label="Password" required>
                            </v-text-field>

                            <v-btn round right color="primary">Login</v-btn>
                        </v-form>
                    </v-flex>
                </v-card>
            </v-layout>
        </v-container>
    </div>
</template>

<script>
export default {
    name: 'login'
}
</script>
<style>
    #formBody{
        border-radius: 15px;
    }
   

</style>
