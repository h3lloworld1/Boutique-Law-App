<template>
  <div>
   <div>
    <b-navbar class="fixed-top" toggleable="lg" variant="" style="background: linear-gradient(#e6e6e6, #ffffff); ">
      <div class="container">
      <b-navbar variant="" type="">
    <b-navbar-brand v-on:click="scroll(1)" style="cursor: pointer">
      <span class="brand-name">Boutique <span style="color: #CC0000;">&</span> firm</span>
    </b-navbar-brand>
  </b-navbar>
      

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto" >
          <b-nav-item v-on:click="scroll(2)"><span class="txt">PRACTISE AREAS</span></b-nav-item>
          <b-nav-item v-on:click="scroll(3)"><span class="txt">OUR VISION</span></b-nav-item>
          <b-nav-item v-on:click="scroll(4)"><span class="txt">ATTORNEYS</span></b-nav-item>
          <b-nav-item v-on:click="scroll(5)"><span class="txt">CONTACT</span></b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </div>
  </b-navbar>
</div>
</div>

</template>

<script>
export default {
  name: 'NavBar',
  props: {
    msg: String
  },
  methods : {
    scroll(id) {  
      document.getElementById(id).scrollIntoView({
        behavior: "smooth"
      });
    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600&display=swap');
.txt {
  font-family: 'raleway';
  font-size: 13px;
  padding: 0px 10px;
  color: black;
  font-weight: lighter;
  font-weight: normal;
}

.brand-name {
  font-size: 24px;
  font-family: 'Dancing Script', cursive;
  font-weight: 600;
}

</style>
