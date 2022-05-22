<template>
  <div class="container-fluid parallax">
      
  </div>
</template>

<script>
export default {
  name: 'ImgA',
  props: {
    msg: String
  }
}
</script>
  
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.parallax {
  background-image: url("https://static.wixstatic.com/media/5bfb6f_bb013bf1966340ceb9a576d68aa42273.jpg") ;
  height: 771px;
  box-shadow: inset 0 0 0 1000px rgba(105, 99, 42, 0.3);

   /* parallax */

  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 768px) {
.parallax {
  background-image: url("https://static.wixstatic.com/media/5bfb6f_bb013bf1966340ceb9a576d68aa42273.jpg") ;
  height: 450px;
  box-shadow: inset 0 0 0 1000px rgba(105, 99, 42, 0.3);

   /* parallax */


}
}




</style>
