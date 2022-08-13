<template>
    <div class="card-group">
        <div class="card" :class="'card-info-'+ card.id" v-for="card in cardConfig" :key="card.id">
            <div class="card-container" :class="(card.id%2 === 0)?'alt-card-container':''">
                <div class="row card-header">
                    <div class="col-12">
                        <!-- CARD IMAGE -->
                        <div class="card-image">
                            <img :src="card.url" :class="card.imageClass" >
                        </div>
                    </div>
                </div>
                <div class="row card-body">
                    <div class="col-12">
                        <!-- CARD TITLE -->
                        <div class="card-title title-4" >
                            {{card.title}}
                        </div>
                    </div>
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

    @media only screen and (max-width: 860px) {
        .card-group{
            float: left;
        }
        .card{
            width: 100%;
            margin-top: 3rem;
        }
        .card-container{
            height: 100%;
            width:100%;
            padding-left: 10rem;
        }

        .alt-card-container{
            padding-left: 5rem;
            padding-top: 0px;
        }

        .row.card-body,.card-header{
            float: left;
        }
        .row.card-body{
            width: 370px;
            padding: 1rem 0rem;
        }
        .row.card-header{
            width: 180px;
        }
    }

    @media only screen and (max-width: 480px) {
        .card-container,.alt-card-container{
            padding: 0px;
            float: inherit;
        }
        .row.card-header{
            width: 100%;
        }
        .card-image{
            width: 120px;
            height: 124px;
            display: inline-block;
            padding: 0px;
        }
        .card-image .passions{
            width: 70px;
            height: 80px;
            margin-top: 22px;
            margin-left: 11px;
        }
        .card-image .freedom{
            width: 70px;
            height: 80px;
            margin-top: 22px;
            margin-left: 0px;
        }

        .card-image .lifestyle{
            width: 70px;
            height: 80px;
            margin-top: 22px;
            margin-left: 0px;
        }

        .card-image .anywhere{
            width: 70px;
            height: 60px;
            margin-top: 30px;
            margin-left: 5px;
        }
        .card-image img{
            width: 100%;
        }
        .card-title{
            text-align: center;
        }
        

        .card-description{
            padding-top:1rem;
            width: 340px;
            text-align: center;
            display: inline-block;
        }
    }
</style>