<template>
    <div class="pricing-container">
        <div class="row">
            <div class="pricing-head">
                <div class="pricing-title">
                    Our pricing plans
                </div>
                <div class="pricing-description description-text">
                    We only make money when our creators make money. Our plans are always affordable, and 
                    it’s completely free to get started.
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col-6">
                <div class="princing-container-free">
                    <div class="plan-container">
                        <div class="row">
                            <div class="plan-title">
                                Dip your toe
                            </div>
                        </div>
                        <div class="row">
                            <div class="plan-description">
                                Just getting started? No problem at all! Our free plan will take you a long way.
                            </div>
                        </div>
                        <div class="row">
                            <div class="plan-price">Free</div>
                        </div>
                        <div class="row">
                            <div class="plan-content">
                                <div class="plan-content-list">
                                    <div class="plan-content-item"><check-icon/>Unlimited products</div>
                                    <div class="plan-content-item"><check-icon/>Basic analytics</div>
                                    <div class="plan-content-item"><check-icon/>Limited marketplace exposure</div>
                                    <div class="plan-content-item"><check-icon/>10% fee per transaction</div>
                                </div> 
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-6">
                <div class="princing-container-basic">
                    
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import CheckIcon from '../components/CheckIcon.vue'
export default {
    components:{
        CheckIcon,
    }
}
</script>

<style>
    .pricing-container{
        text-align: center;
    }
    .pricing-head{
        width: 540px;
        height: 118px;
        display: inline-block;
    }
    .pricing-title{
        font-size: 32px;
        font-weight: 800;
        line-height: 43.71px;
        text-align: center;
    }

    .pricing-description{
        text-align: center;
        margin-top: 2rem;
    }

    .pricing-container-free .plan-container{
        background-color: #093F68;
        width: 445px;
        height: 448px;
    }
</style>