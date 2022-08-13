<template>
  <div class="pricing-container">
        <div class="row">
            <div class="princing-container-body">
                <div class="plan-container">
                    <div class="row p-title">
                        <div class="plan-title title-4">
                            {{pricingTitle}}
                        </div>
                    </div>
                    <div class="row p-description">
                        <div class="plan-description">
                            {{pricingDescription}}
                        </div>
                    </div>
                    <div class="row p-price">
                        <div >
                            <div class="plan-price title-2">{{pricingValue}}</div>
                            <div class="plan-price-period" v-if="pricingPeriod!=''">/{{pricingPeriod}}</div>
                        </div>
                    </div>
                    <div class="row p-content">
                        <div class="plan-content">
                            <div class="plan-content-list">
                                <div class="plan-content-item" v-for="(content,idx) in pricingContent" :key="idx">
                                    <div class="content-item-icon"><check-icon/> </div>
                                    <div class="content-item-content">{{content}}</div>
                                </div>
                            </div> 
                        </div>
                    </div>
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
    },
    props:[
        'pricingTitle',
        'pricingDescription',
        'pricingValue',
        'pricingContent',
        'pricingPeriod'
    ],
    data(){
        return {
        }
    }
}
</script>

<style>
    .pricing-container{
        width: 445px;
        height: 448px;
        padding: 6rem 2rem;
        border-radius: 8px;
    }

    .princing-container-body{
        text-align: left;
    }

    .p-description{
        padding-top: 22px;
        text-align: left;
    }

    .p-price{
        padding-top: 44px;
    }

    .p-content{
        padding-top:1rem
    }
    .plan-title{
        width: 127px;
        height: 25px;
        font-weight: 800;
        font-size: 18px;
        line-height: 25px;
    }
    .plan-description{
        display: inline-block;
        width: 369px;
        height: 50px;
        opacity: 59.73%;
        font-size: 15px;

    }

    .plan-price{
        float: left;
        width: 141px;
        height: 55px;
        font-weight: bold;
        font-size: 40px;
        line-height: 54.64px;
    }
    .plan-price-period{
        float: left;
        width: 56px;
        height: 25px;
        opacity: 60%;
        font-weight: 500;
        font-size: 15px;
        line-height: 25px;
        padding: 15px;
    }

    .plan-content .plan-content-item {
        width: 340px;
        height: 25px;
        font-weight: 500;
        font-size: 15px;
        line-height: 25px;
        float: left;
        width: 100%;
        margin-top: 15px;
    }
    .plan-content-item div{
        float: left;
    }
    .content-item-content{
        margin-left: 20px;
    }

    @media only screen and (max-width: 480px) {
        .p-content,.p-price{
            padding-top: 10px;
        }
        .plan-price{
            width: 120px;
        }
        .plan-price-period{
            padding-left: 0px;
        }
        .pricing-container{
            width: 100%;
        }
    }
</style>