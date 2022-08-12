<template>
   <div class="row">
        <div class="col-4">
            <div class="hero-background hero-left"></div>
        </div>
        <div class="col-4">
            <div class="hero-center">
                <div class="row">
                    <div class="col-12">
                        <div class="title">
                            Get paid for the work
                            you love to do.
                        </div>
                    </div>
                </div>
                <div class="row">
                    <div class="col-12">
                        <div class="simple-text">
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
        <div class="col-4">
            <div class="hero-background hero-right">
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
    }

    .hero-right{
        background-image: url('../assets/images/illustration-hero-right.svg');
        background-position: center;
        background-repeat: no-repeat;
    }


    .hero-center{
        background-image: url('../assets/images/bg-hero-squiggle.svg');
        background-position: center;
        background-repeat: no-repeat;
        text-align: center;
    }

    .simple-text{
        color: #777F98;
    }

    .scroll-row{
        margin-top: 3rem;
    }
</style>