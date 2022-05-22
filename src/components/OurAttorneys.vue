<template>
    <div id="4" class="container-fluid" style="background-color: #eaf4f6; padding-bottom: 100px">
       <div class="container">
            <div class="t-1">OUR ATTORNEYS</div>
                <div class="row justify-content-center" style="text-align: center">
                    <div class="col-lg-4 col-md-6 col-sm-12">
                        <div class="flip-card">
                            <div class="flip-card-inner">
                                <div class="flip-card-front">
                                <img src="https://static.wixstatic.com/media/5bfb6f_5577b01919214f47ad5236247965ec04.jpg/v1/fill/w_193,h_220,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/5bfb6f_5577b01919214f47ad5236247965ec04.jpg" alt="Avatar" style="width:193px;height:220px;">
                                </div>
                                <div class="flip-card-back">
                                <h5>AIDEN WALTERS</h5>
                                <p class="p1">PARTNER</p>
                                <div class="line"></div>
                                <p class="mb-0 p2" p2>Tel: 123-456-7890</p>
                                <p class="p2">example@gmail.com</p>
                        </div>
                    </div>
                </div>
            </div>
            
                <div class="col-lg-4 col-md-6 col-sm-12">
                    <div class="flip-card">
                        <div class="flip-card-inner">
                                <div class="flip-card-front">
                                <img src="https://static.wixstatic.com/media/5bfb6f_60ff20475dbc447f92c81fdcc6a6a7c1.jpg/v1/fill/w_193,h_220,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/5bfb6f_60ff20475dbc447f92c81fdcc6a6a7c1.jpg">
                                </div>
                                <div class="flip-card-back">
                                <h5>AIDEN WALTERS</h5>
                                <p class="p1">PARTNER</p>
                                <p class="mb-0 p2">Tel: 123-456-7890</p>
                                <p class="p2">example@gmail.com</p>
                        </div>
                    </div>
                </div>
            </div>

                <div class="col-lg-4 col-md-6 col-sm-12">
                    <div class="flip-card">
                        <div class="flip-card-inner">
                                <div class="flip-card-front">
                                <img src="https://static.wixstatic.com/media/5bfb6f_1cafad56984b4997bd73792b008c6fc3.jpg/v1/fill/w_193,h_220,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/5bfb6f_1cafad56984b4997bd73792b008c6fc3.jpg">
                                </div>
                                <div class="flip-card-back">
                                <h5>AIDEN WALTERS</h5>
                                <p class="p1">PARTNER</p>                               
                                <p class="mb-0 p2">Tel: 123-456-7890</p>
                                <p class="p2">example@gmail.com</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
    
</template>

<script>
export default {
  name: 'OurAttorneys',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

* {
    font-family: 'open sans', sans-serif;
}

.t-1 {
    text-align: center; 
    padding-top: 7%; 
    padding-bottom: 5%;
    font-family: 'raleway', sans-serif;
    font-size: 42px;
    color: #00305b;
}

h5 {
    padding-top: 4%;
    font-size: 20px;
    color: #00305b;
}

.p1 {
    font-size: 16px;
    color: #0f4c85;
}

.p2 {
    font-size: 16px;
    color: #00305b;
}

.p1 {
    border-bottom: 1px solid rgba(0,48,91, 1);
}

</style>
