<template>
  <div id="1" class="container-fluid showcase parallax">
       <div  v-if="txt > 767" style="padding-left: 20%; padding-top: 330px;">
            <span><h1 class="h-text font-weight-bold">BOUTIQUE</h1></span> 
            <span><h1 class="h-text font-weight-thin">LAW FIRM</h1></span> 
            <div style="padding-top: 10px;"><span><h3 class="p-text">Specializing in Commercial Law &</h3> </span> 
            <span><h3 class="p-text"> Litigation, Insolvency & Fraud</h3></span></div>
       </div>
            <div class="text-left" style="padding-top: 50%;" v-else>
            <span><h1 class="h-text font-weight-bold">BOUTIQUE</h1></span> 
            <span><h1 class="h-text font-weight-thin">LAW FIRM</h1></span> 
            <div style="padding-top: 10px;"><span><h3 class="p-text">Specializing in Commercial Law &</h3> </span> 
            <span><h3 class="p-text"> Litigation, Insolvency & Fraud</h3></span></div>
       </div>
  </div>
</template>

<script>
export default {
  name: 'ShowCase',
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
.showcase {
  background-image: linear-gradient(to right, rgba(0, 48, 91, 0.6), rgba(0, 48, 91, 0.6) 40%, transparent 50%), url("https://static.wixstatic.com/media/5bfb6f_a463284fd84145f292a32dc0f0e0cc31.jpg");
  height: 870px;
  background-size: cover;
  box-shadow: inset 0 0 0 1000px rgba(0, 48, 91, 0.3); 
}

.h-text {
  font-family: 'raleway', sans-serif;
  font-size: 42px;
  color: white
}

.p-text {
  font-family: 'open sans', sans-serif;
  font-size: 18px;
  color: white;
}

.parallax {
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
} 

/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
.parallax {
  background-image: linear-gradient(to left, rgba(0, 48, 91, 0.6), rgba(0, 48, 91, 0.6) 57%, transparent 50%), url("https://static.wixstatic.com/media/5bfb6f_a463284fd84145f292a32dc0f0e0cc31.jpg/v1/fill/w_320,h_330,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/5bfb6f_a463284fd84145f292a32dc0f0e0cc31.jpg");
  height: 550px;
  box-shadow: inset 0 0 0 1000px rgba(0, 48, 91, 0.3);
}
}



</style>
