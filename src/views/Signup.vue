<template>
    <div>

        <v-container grid-list-xl>
            <v-layout row wrap>
                <v-card id="carta">
                    <v-flex xs10 offset-xs1>
                        <v-form v-model="valid">
                            <h1>Registrarse en Tuister</h1>

                            <v-text-field v-model="name" label="Name" :rules="nameRules" required>
                            </v-text-field>

                            <v-text-field v-model="nickname" label="Nickname" :rules="nickRules" required>
                            </v-text-field>

                            <v-text-field type="email" v-model="email" label="Email" :rules="emailRules" required>
                            </v-text-field>

                            <v-text-field type="password" v-model="password" :counter="8" label="Password" :rules="passRules" required>
                            </v-text-field>

                            <v-text-field type="password" v-model="c_password" :counter="8" label="Confirm password" :rules="passRules" required>
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
    name: 'signup',
    data() {
        return {
            valid: false,
            name: '',
            nameRules:[
                v => !!v || 'Name is required',
            ],
            nickname: '',
            nickRules:[
                v => !!v || 'Nickname is required',
            ],
            email: '',
            emailRules:[
                v => !!v || 'Email is required',
                v => /.+@.+/.test(v) || 'E-mail must be valid'
            ],
            password: '',
            c_password: '',
            passRules:[
                v => !!v || 'Password is required',
                v => v.length >= 8 || 'Password must be at least 8 characters',
                // v => this.password || 'The password does not match'
            ],
            
        }
    },
}
</script>
<style>
    #carta{
        border-radius: 15px;
    }

</style>
