<template>
    <div class="service-section">
        <card-info
            :card-config="cardConfig"
        ></card-info>
    </div>
</template>

<script>
import CardInfo from '../components/CardInfo.vue'

export default {
    data(){
        return {
            cardConfig:[
                {
                    id:1,
                    url:require('../assets/images/illustration-passions.svg'),
                    title:'Indulge your passions',
                    description:"Your passions shouldn't be just for the weekend. Earn a living doing what you love.",
                },
                {
                    id:2,
                    url:require('../assets/images/illustration-financial-freedom.svg'),
                    title:'Gain financial freedom',
                    description:"Start making money work for you. There’s nothing quite like earning while you sleep.",
                },
                {
                    id:3,
                    url:require('../assets/images/illustration-lifestyle.svg'),
                    title:'Choose your lifestyle',
                    description:"Own your daily schedule. Fancy a lie-in? Go for it! Take charge of your week.",
                },
                {
                    id:4,
                    url:require('../assets/images/illustration-work-anywhere.svg'),
                    title:'Work from anywhere',
                    description:"Selling online means not being pinned down. Want to work AND travel? Go for it!",
                }
            ],
        };
    },
    components:{
        CardInfo,
    }
}
</script>

<style>
    .service-section{
        text-align: center;
        display: inline-block;
        width: 100%;
    }
</style>