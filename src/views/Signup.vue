<template>
    <div>
        <v-container grid-list-xl>
            <v-layout row wrap>
                <v-card id="carta">
                    <v-flex xs10 offset-xs1>
                        <v-form v-on:submit.prevent="validateBeforeSubmit" v-if="!formSubmitted">

                            <h1>Registrarse en Tuister</h1>

                            <v-text-field  label="Name" name="name" v-validate="'required'"></v-text-field>
                            <span>{{ errors.first('name') }}</span>

                            <v-text-field label="Nickname" name="nickname" v-validate="'required'"></v-text-field>
                            <span>{{ errors.first('nickname') }}</span>

                            <v-text-field type="email"  label="email" name="email" v-validate="'required|email'"></v-text-field>
                            <span>{{ errors.first('email') }}</span>

                            <v-text-field type="password" :counter="8" label="Password" name="password" v-validate="'required|min:8'" ref="password"></v-text-field>
                            <span v-if="errors.has('password')">{{ errors.first('password') }}</span>

                            <v-text-field type="password" :counter="8" label="Confirm password" data-vv-as="password" name="pass_confirmed" v-validate="'required|confirmed:password'"></v-text-field>
                            <!-- <span v-if="errors.has('pass_confirmed')">{{errors.first('pass_confirmed')}}</span> -->
                            
                            <v-btn round right color="primary" type="submit">Login</v-btn>
                        </v-form>

                    </v-flex>
                </v-card>
            </v-layout>
        </v-container>
    </div>
</template>

<script>
import VeeValidate from 'vee-validate';
import Vue from 'vue';
Vue.use(VeeValidate);

export default {
    name: 'signup',
    data() {
        return {

            data() {
                return {

                    formSubmitted: false
                    
                }
            },
           
            
        }
         
    },
    methods: {

        validateBeforeSubmit(e) {
        this.$validator.validateAll();
        if (!this.errors.any()) {
            this.submitForm()
        }
      },
      submitForm(){
      this.formSubmitted = true
      },
    },
}
</script>
<style>
    #carta{
        border-radius: 15px;
    }
    span{
        color: red;
    }

</style>
