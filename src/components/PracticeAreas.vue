<template>
  <div id="2" class="container-fluid bk-color">
    <div class="container" style="padding-top: 80px; padding-bottom: 100px;">
      <div class="row">
        <div class="col-lg-6 col-md-6 col-sm-12">
          <span v-if="txt > 767" class="row justify-content-center">
            <h2 class="font-weight-bold pl-3 h-text" style="padding-top: 10px;">PRACTICE <h2 class="font-weight-thin h-text">AREAS</h2></h2></span>

            <span v-else class="row">
            <h2 class="font-weight-bold pl-3 h-text">PRACTICE <h2 class="font-weight-thin h-text">AREAS</h2></h2>
            </span>

        </div>
          <div class="col-lg-3 col-md-3 col-sm-12">
              <h3 class="head-t">LITIGATION</h3>  
              <p class="pt-3 p-t"> Lorem ipsum dolor sit amet consectetur adipisicing elit. Totam, recusandae.</p>
              <h3 class="head-t">INSOLVENCY</h3>
              <p class="pt-3 p-t"> Lorem ipsum dolor sit amet consectetur, adipisicing elit. Provident, eum tempora?</p>
              <h3 class="head-t">DISPUTE RESOLUTION</h3>
              <p class="pt-3 p-t">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Saepe iusto esse delectus recusandae.</p>
          </div>
          <div class="col-lg-3 col-md-3 col-sm-12">
              <h3 class="head-t">BUSINESS</h3>
              <p class="pt-3 p-t"> Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam, magnam.</p>
              <h3 class="head-t">FRAUD</h3>
               <p class="pt-3 p-t"> Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium, voluptatem!</p>
              <h3 class="head-t">TAX</h3>
              <p class="pt-3 p-t"> Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta.</p>
            </div>
      </div>
    </div>
  </div>
  
</template>

<script>
export default {
  name: 'PracticeAreas',
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

* {
  font-family: 'open sans', sans-serif;
  color: #00305B;
}

.h-text {
  font-family: 'raleway', sans-serif;
  font-size: 42px;;
}

.head-t {
  font-size: 20px;
  padding-top: 20px;
}

.p-t {
  font-size: 14px;
  color: #0F4c85;
}

#square {
  width: 10px;
  height: 10px;
  background: #0f4c85;
}

.bk-color {
 background: linear-gradient(to right,  #EAF4F6 0%,#EAF4F6 43%,#f6f6f6 43%,#f6f6f6 100%)
}

@media only screen and (max-width: 767px) {
  .bk-color {
  background: linear-gradient(to bottom,  #EAF4F6 0%,#EAF4F6 19%,#f6f6f6 19%,#f6f6f6 100%)
  }

}
</style>
