<template>
    <div class="row">
        <div class="col-12">
            <div class="contact-section">
                <contact-form></contact-form>
            </div>
        </div>
    </div>
</template>

<script>
import ContactForm from './ContactForm.vue'
export default {
    components:{
        ContactForm,
    }
}
</script>

<style>
    .contact-section{
        width: 100%;
        height: 230px;
        padding-top: 15px;
        background-image: url('../assets/images/bg-footer-squiggle.svg');
        background-position: center;
        background-repeat: no-repeat;
    }
    @media only screen and (max-width: 860px) {
        .contact-section{
            background-size: 775px 168px;
        }
    }
    @media only screen and (max-width: 480px) {
        .contact-section{
            margin-top: 5rem;
            background-size: 475px 100px;
            background-position: 0px 45px;
        }

    }
</style>