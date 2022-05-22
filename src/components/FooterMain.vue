<template>
<div class="container-fluid" style="padding-top: 40px; padding-bottom: 23px;">
  <div class="container">
     <div class="row justify-content center">
        <div class="col-6">
           <p class="text">© {{new Date().getFullYear()}} MySite. All rights reserved</p>
        </div>

        <div class="col-6" style="align-content: end">
          <div class="logo"> </div>
          <div class="logo2"></div>
          
        </div>
    </div>
  </div>
</div>
</template>


<script>
export default {
  name: 'FooterMain',
  data(){
    return{
      windowHeight: '',
      txt: window.innerWidth,
    }
  },
   watch: {
        windowHeight(newHeight) {
            this.txt = newHeight;
        }
    },

    mounted() {
        this.$nextTick(() => {
            window.addEventListener('resize', this.onResize);
        })
    },

    beforeDestroy() { 
        window.removeEventListener('resize', this.onResize); 
    },

    methods: {  
        onResize() {
            this.windowHeight = window.innerWidth
        }
    },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.text {
  color: #0f4c85;
}

.logo {
  background-image: url('https://static.wixstatic.com/media/48a2a42b19814efaa824450f23e8a253.png/v1/fill/w_23,h_23,al_c,usm_0.66_1.00_0.01,enc_auto/48a2a42b19814efaa824450f23e8a253.png');
  background-size: cover;
  width: 23px;
  height: 23px;
  float: right;

}

.logo2{
  background-image: url('https://static.wixstatic.com/media/9c4b521dd2404cd5a05ed6115f3a0dc8.png/v1/fill/w_23,h_23,al_c,usm_0.66_1.00_0.01,enc_auto/9c4b521dd2404cd5a05ed6115f3a0dc8.png');
  background-size: cover;
  width: 23px;
  height: 23px;
  float: right;
  margin-right: 5px;
}

.container-fluid {
  bottom: 0px;
}
</style>
