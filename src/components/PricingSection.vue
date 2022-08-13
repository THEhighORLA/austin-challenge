<template>
    <div class="pricing-section">
        <div class="row">
            <div class="pricing-head">
                <div class="pricing-title title-3">
                    Our pricing plans
                </div>
                <div class="pricing-description description-text">
                    We only make money when our creators make money. Our plans are always affordable, and 
                    it’s completely free to get started.
                </div>
            </div>
        </div>
        <div class="row">
           <div class="col-12 pricing">
                <div class="pricing-tag pricing-container-free">
                    
                    <div class="pricing-background">
                        <div class="pricing-free-icon">
                        <img src="../assets/images/icon-free.svg">
                    </div>
                    </div>
                    <pricing-container
                        :pricingTitle="pricingTitleFree"
                        :pricingDescription="pricingDescriptionFree"
                        :pricingValue="pricingValueFree"
                        :pricingPeriod="''"
                        :pricingContent="pricingContentFree"
                    ></pricing-container>
                </div>
                <div class="pricing-tag pricing-container-basic">
                    
                    <div class="pricing-background">
                        <div class="pricing-free-icon">
                            <img src="../assets/images/icon-paid.svg">
                        </div>
                    </div>
                    <pricing-container
                        :pricingTitle="pricingTitleBasic"
                        :pricingDescription="pricingDescriptionBasic"
                        :pricingValue="pricingValueBasic"
                        :pricingPeriod="pricingPeriodBasic"
                        :pricingContent="pricingContentBasic"
                    ></pricing-container>
                </div>
           </div>
        </div>
    </div>
</template>

<script>
import PricingContainer from '../components/PricingContainer.vue'

export default {
    components:{
        PricingContainer,
    },
    data(){
        return {
            //Configuration Variables for free pricing
            pricingTitleFree:'Dip your toe',
            pricingDescriptionFree:'Just getting started? No problem at all! Our free plan will take you a long way.',
            pricingValueFree:'Free',
            pricingContentFree:[
                'Unlimited products',
                'Basic analytics',
                'Limited marketplace exposure',
                '10% fee per transaction',
            ],

            //Configuration Variables for basic pricing
            pricingTitleBasic:'Dive right in',
            pricingDescriptionBasic:'Ready for the big time? Our paid plan will help you take your business to the next level.',
            pricingValueBasic:'$25.00',
            pricingPeriodBasic:"month",
            pricingContentBasic:[
                'Custom domain',
                'Advanced analytics and reports',
                'High marketplace visibility',
                '5% fee per transaction',
            ],
        };
    }
}
</script>

<style>
    .pricing{
        margin-top: 5rem;
    }
    .pricing-section{
        text-align: center;
        height: 100%;
        display: inline-block;
    }
    .pricing-head{
        width: 550px;
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

    .pricing-tag{
        float: left;
    }

    .pricing-container-free .pricing-free-icon{
        text-align: left;
        margin: -1.5rem 2rem;
    }

    .pricing-container-basic .pricing-free-icon{
        text-align: left;
        margin: -2rem 2rem;
    }

    .pricing-container-free .pricing-background{
        position: absolute;
        width: 445px;
        height: 480px;
        background-color: #093F68;
        z-index: -1;
        border-radius: 8px;
        margin: 17.5px 0px;
    }

    .pricing-container-basic{
        padding: 0px 0px;
        margin-left: 3rem;
    }

    .pricing-container-basic .pricing-background{
        position: absolute;
        width: 445px;
        height: 515px;
        background-color: #3EE9E5;
        z-index: -1;
        border-radius: 8px;
    }

    .pricing-container-free .pricing-container{
        /* background-color: #093F68; */
        background-size: 445px;
        color: #fff;
        width: 445px;
        height: 448px;
    }

    .pricing-container-basic .pricing-container{
        /* background-color: #3EE9E5; */
        color: #080C20;
        width: 445px;
        height: 448px;
    }

    .pricing-container-free img{
        filter: brightness(0) invert(1);
    }

    @media only screen and (max-width: 860px) {
        .pricing-container-basic{
            padding: 0px 0px;
            margin-left: 0rem;
            margin-top: 5rem;
        }
        .col-12.pricing{
            margin-left: auto;
            margin-right: auto;
            width: 60%;
            float: inherit;
        }
    }
    @media only screen and (max-width: 480px) {
        .pricing-section{
            display: inherit;
        }
        .pricing-head{
            width: 340px;
        }
        .col-12.pricing{
            margin: 0px;
            width: 100%;
            padding-top: 3rem;
        }

        .pricing-container-basic{
            margin-top: 7rem;
        }

        .pricing-container-free .pricing-background,.pricing-container-basic .pricing-background{
            width: 95%;
        }

        .plan-description{
            width: 275px;
        }

    }
</style>