<template>
  <div id="5" class="container-fluid showcase parallax" style="padding-top: 100px; padding-bottom: 100px">
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-lg-12 col-xl-6 col-md-12 col-sm-12">
                <h1 style="font-size: 42px">CONTACT <br> KNOLL & <br> WALTERS</h1>
            </div>

            <div class="col-lg-12 col-xl-6 col-md-12 col-sm-12">
                <h4 style="font-size: 20px;"><span style="font-size: 20px" class="font-weight-bold">OUR</span> ADRESS</h4>
                <p class="mb-0 pt-3">Example adress</p>
                <p class="mb-0"><span class="font-weight-bold">Email:</span> example@gmail.com</p>
                <p><span class="font-weight-bold">Tel:</span>  123-456-7890</p>
                <router-link to="/about">
                    <a style="font-size: 20px" >Click here to Find Us</a>
                </router-link>
                <p class="pt-5">For any general inquiries, please fill in the following contact form:</p>
            </div>
            
        </div>

        <div class="row">
            <div class="col-lg-12 col-xl-6 col-md-12 col-sm-12">
                
            </div>
                
            <div class="col-lg-12 col-xl-3 col-md-12 col-sm-12">
                <p class="mb-0">First Name*</p>
                <input class="form-control" type="text" placeholder="Enter Name here" aria-label="default input example">
                <p class="pt-3 mb-0">Last Name*</p>
                <input class="form-control" type="text" placeholder="Enter Last Name here" aria-label="default input example">
                <p class="pt-3 mb-0">Email*</p>
                <input class="form-control" type="text" placeholder="Enter Email here" aria-label="default input example">
                <p class="pt-3 mb-0">Subject*</p>
                <input class="form-control" type="text" placeholder="Enter subject here" aria-label="default input example">
            </div>

                
            <div class="col-lg-12 col-xl-3 col-md-12 col-sm-12">
                <p class="mb-0">Message*</p>
                <div class="form-floating">
                <textarea class="form-control" placeholder="Leave a comment here" id="floatingTextarea2" style="height: 273px"></textarea>
  
</div>
            </div>
            </div>

            <div class="row justify-content-center">
                <div class="col-lg-12 col-xl-6 col-md-12 col-sm-12">
                    
                </div>

                <div class="col-lg-12 col-xl-6 col-md-12 col-sm-12 pt-3">
                    <input type="submit" id="submit-btn" value="Submit"  style="height:35px; width:100%; color: white" />
                </div>
            </div>
        <a v-if="scrspy" id="back2Top" @click="scrollTo" title="Back to top">&#10148;</a>
        
    </div>

   
  </div>
  
</template>

<script>


export default {
  name: 'ContactS',
  data(){
      return{
         scrspy: '' ,
      }
    },
    methods:{
    scroll () {
        window.onscroll = () => {
        let bottomOfWindow = Math.max(window.pageYOffset, document.documentElement.scrollTop, document.body.scrollTop) + window.innerHeight === document.documentElement.offsetHeight
        this.scrspy= bottomOfWindow;
            }
    },
    scrollTo() {           
        window.scroll({
        top: 0,
        behavior: 'smooth'
  }) 
            
        }
    },

    mounted(){
        this.scroll()
    },

  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

* {
    color: white;
    font-family: 'open-sans', sans-serif;
    font-size: 16px;
}

.showcase {
background-image: linear-gradient(to right, rgba(0, 48, 91, 0.7), rgba(0, 48, 91, 0.7) 100%, transparent 70%), url("https://static.wixstatic.com/media/5bfb6f_c9a631e8e43443cb9d7ad97133d9d83d.jpg/v1/fill/w_1903,h_809,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/5bfb6f_c9a631e8e43443cb9d7ad97133d9d83d.jpg");
background-size: cover;
}

a {
    color: white;
    text-decoration: underline;
}

#submit-btn {
    background-color: #0f4c85;
    border: 1px solid white;
}

#submit-btn:hover {
    background-color: #00305b;
}

.parallax {
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
} 

#back2Top {
    width: 60px;
    line-height: 60px;
    overflow: hidden;
    z-index: 999;
    cursor: pointer;
    -moz-transform: rotate(270deg);
    -webkit-transform: rotate(270deg);
    -o-transform: rotate(270deg);
    -ms-transform: rotate(270deg);
    transform: rotate(270deg);
    position: fixed;
    bottom: 25px;
    right: 20px;
    background-color: transparent;
    color: #00305b;
    
    font-size: 60px;
    text-decoration: none;
    
}
#back2Top:hover {
    background-color: transparent;
    color: #0f4c85;
}

@media only screen and (max-width: 1536px) {

#back2Top {
    display: none;

    }
}


@media only screen and (max-width: 768px) {
.ppr{
    padding-left: 0;
    }
}

</style>
