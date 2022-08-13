<template>
   <div class="row">
        <div class="col-12 hero-landing-mobile">
            <div class="hero-background hero-left"></div>
            <div class="hero-background hero-right"></div>
        </div>
        <div class="col-12 hero-landing">
            <div class="hero-center">
                <div class="row">
                    <div class="col-12">
                        <div class="title-1">
                            Get paid for the work
                            you love to do.
                        </div>
                    </div>
                </div>
                <div class="row">
                    <div class="col-12">
                        <div class="description-text">
                            The 9-5 grind is so last century. We believe in living life on your 
                            own terms. Whether you’re looking to escape the rat race or set up 
                            a side hustle, we’ve got you covered.
                        </div>
                    </div>
                </div>
                <div class="row scroll-row">
                    <div class="row-12">
                        <div class="scroll-icon">
                            <img src="../assets/images/icon-scroll.svg">
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
    </div>
</template>

<script>
export default {

}
</script>

<style>
    .title{
        font-size: 48px;
        font-weight: 800;
    }
    .header{
        position: relative;
        height: 100%;
        width: 100%;
        background-size: auto;
        
    }
    .hero-background{
        height: 460px;
        width: 100%;
    }
    .hero-left{
        
        background-image: url('../assets/images/illustration-hero-left.svg');
        background-position: center;
        background-repeat: no-repeat;
        max-width: 100%;
    }

    .hero-right{
        background-image: url('../assets/images/illustration-hero-right.svg');
        background-position: center;
        background-repeat: no-repeat;
        max-width: 100%;
    }

    .hero-landing{
        text-align: center;
        background-image: url('../assets/images/illustration-hero-left.svg'),url('../assets/images/bg-hero-squiggle.svg'),url('../assets/images/illustration-hero-right.svg');
        background-position: left, center, right;
        background-repeat: no-repeat, no-repeat, no-repeat;
        background-position:0px 0px,50% 0px,100% 0px ;
        background-size:410px 100%, 550px 100%,400px 100%;
    }
    .hero-center{
        
        display: inline-block;
        height: 400px;
        padding-top: 3rem;
        width: 730px;
    }


    .simple-text{
        color: #777F98;
    }

    .scroll-row{
        margin-top: 3rem;
    }

    .hero-landing-mobile{
        display: none;
    }
    @media only screen and (max-width: 860px) {
        .hero-landing {
            background-size:310px 100%, 450px 100%,300px 100%;
            background-position:-190px 0px,50% 0px,650px 0px ;
        }

        .hero-center{
            width: 530px;
        }
    }

    @media only screen and (max-width: 480px) {
        .hero-center{
            width: 310px;
            padding-top: 1rem;
        }
        .hero-center .description-text{
            padding-top: 1rem;
        }
        .hero-landing{
            background:none
        }
        .hero-landing-mobile{
            display: block;
        }
        .hero-background{
            width: 50%;
            height: 250px;
            float: left;
        }
        .hero-landing-mobile .hero-left{
            background-size: 100% 200px;
        }
        .hero-landing-mobile .hero-right{
            background-size: 100% 200px;
        }
    }
</style>