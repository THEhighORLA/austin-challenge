<template>
    <div>
        <div class="content">
            <!-- Logo -->
            <div class="col-12">
                <div class="logo">
                    <img src="../assets/images/logo.svg">
                </div>
            </div>
            
            <!-- Main Section -->
            <div class="row section">
                <div class="col-12">
                   <main-section></main-section> 
                </div>
            </div>
            <!-- Services Summary -->
            <div class="row section">
                <div class="col-12">
                    <service-section></service-section>
                </div>
            </div>
            <!-- Pricing Plans -->
            <div class="row section">
                <div class="col-12">
                    <pricing-section></pricing-section>
                </div>
            </div>
            <!-- Contact Form -->
            <div class="row section">
                <div class="col-12">
                    <contact-section></contact-section>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import MainSection from './MainSection.vue';
import ServiceSection from './ServiceSection.vue';
import PricingSection from './PricingSection.vue';
import ContactSection from './ContactSection.vue'

export default {
    data(){
        return {
            text:"Prueba texto",
        }
    },
    components:{
        MainSection,
        ServiceSection,
        PricingSection,
        ContactSection,
    }
}
</script>

<style>
    .section{
        margin-top: 10rem;
        align-items: center;
    }
</style>