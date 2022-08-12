<template>
    <div class="card-group">
        <div class="card" :class="'card-info-'+ card.id" v-for="card in cardConfig" :key="card.id">
            <div class="card-container" :class="(card.id%2 === 0)?'alt-card-container':''">
                <div class="row ">
                    <div class="col-12">
                        <!-- CARD IMAGE -->
                        <div class="card-image">
                            <img :src="card.url" >
                        </div>
                    </div>
                </div>
                <div class="row">
                    <div class="col-12">
                        <!-- CARD TITLE -->
                        <div class="card-title">
                            {{card.title}}
                        </div>
                    </div>
                </div>
                <div class="row">
                    <div class="col-12">
                        <!-- CARD DESCRIPTION -->
                        <div class="card-description description-text">
                            {{card.description}}
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    // data(){
    //     return {

    //     };
    // },
    props:{
        cardConfig:{
            type:Array,
            default(){
                return [];
            },
        }
    },
}
</script>

<style>
    .card-group{
        display: inline-block;
    }
    .card{
        float: left;
    }

    .card-container{
        width: 255px;
        height: 335px;
    }

    .alt-card-container{
        padding-top: 48px;
    }

    .card-image{
        background-color: #093F6B;
        padding: 28px 43px;
        text-align: center;
        width: 160px;
        height: 164px;
        border-radius: 45px;
    }

    .card-title{
        font-size: 18px;
        font-weight: 800;
        text-align: left;
    }

    .card-description{
        
        justify-content: left;
        text-align: left;
    }
</style>