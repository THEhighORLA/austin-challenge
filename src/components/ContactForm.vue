<template>
    <div class="contact-form">
        <div class="contact-form-title title-5">
            Get notified when we launch
        </div>
        <div class="contact-form-body">
            <form>
                <div class="email-input-group">
                    <input 
                        v-model.trim.lazy="$v.userEmail.$model"
                        class="email-input "
                        placeholder="Email address"
                        type="text"
                    />
                    <div class="error-msg" v-show="stateEmailFormat">Oops! That doesn't look like an email address</div>
                    <div class="error-msg" v-show="stateEmailRequired">Oops! Please add your email</div>
                </div>
                <div class="form-button">
                    <button 
                        type="submit" 
                        @click.prevent="validateForm"
                    >Get notified</button>
                </div>
            </form>
        </div>
    </div>
</template>

<script>
import {required,email} from 'vuelidate/lib/validators'

export default {
    data(){
        return {
            userEmail:"",

        }
    },
    validations:{
        userEmail:{
            required,
            email
        }
    },
    computed:{
        stateEmailRequired(){
            let vUserEmail = this.$v.userEmail;
            return !vUserEmail.required && vUserEmail.$dirty
        },
        stateEmailFormat(){
            let vUserEmail = this.$v.userEmail;
            return !vUserEmail.email && vUserEmail.$dirty
        }
    },
    methods:{
        validateForm(){
            this.$v.$touch()
            if(!this.$v.$error){
                console.log(this.userEmail);
                this.userEmail = "";
                this.$v.$reset();
            }
        }
    }
}
</script>

<style>
    .contact-form-title{
        font-weight: 800;
        font-size: 32px;
        line-height: 43.71px;
        padding: 2rem 2rem;
        
    }

    .contact-form{
        display: inline-block;
    }

    .contact-form-body input{
        padding: 10px;
        width: 320px;
        height: 48px;
        background-color: #093F60;
        border-radius: 24px;
        border: 1px solid #093F60;
        color: #fff;
    }
    .contact-form-body input:focus{
        border: 3px solid #fff;
        color: #fff;
        outline: #fff;
    }

    .contact-form-body input:invalid,.contact-form-body input.invalid{
        border: 3px solid #FF2965;
    }

    .contact-form-body input::placeholder{
        font-style: normal;
        font-weight: 700;
        font-size: 15px;
        line-height: 25px;
        opacity: 1;
    }

    .email-input-group,.form-button{
        float: left;
    }

    .email-input-group .error-msg{
        color:#FF2965;
        font-size: 12px;
        line-height: 25px;
        font-weight: 500;
    }

    .contact-form-body button{
        padding: 10px;
        width: 140px;
        height: 48px;
        border-radius: 24px;
        background-color: #3EE9E5;
        font-weight: bold;
        font-size: 15px;
        line-height: 25px;
        text-align: center;
        color: #093F68;
        border: 0px;
        cursor: pointer;
        float: left;
        margin-left: 15px;
    }

    .contact-form-body button:hover,.contact-form-body button:active{
        outline: 3px solid #3EE9E5;
        background-color: transparent;
        color: #fff;
    }

    @media only screen and (max-width: 480px) {
        .email-input-group{
            float: none;
        }

        .contact-form-body,.email-input-group,.form-button {
            width: 100%;
        }
        .contact-form-body .form-button {
            padding: 5px;
            height: 48px;
            margin-top: 1rem;
        }
        .contact-form-body button{
            width: 320px;
        }
        .contact-form{
            height: 20rem;
        }
    }

</style>