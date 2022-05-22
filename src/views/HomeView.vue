<template>
  <div id="app">
    <ShowCase/>
    <PracticeAreas/>
    <OurVision/>
    <ImgA/>
    <OurAttorneys/>
    <ContactS/>
  </div>
</template>


<script>
import ShowCase from "../components/ShowCase.vue"
import PracticeAreas from "../components/PracticeAreas.vue"
import OurVision from "../components/OurVision.vue"
import ImgA from "../components/ImgA.vue"
import OurAttorneys from "../components/OurAttorneys.vue"
import ContactS from "../components/ContactS.vue"




export default {
  name: 'App',
   data () {
    return {
      greeting: 'Hello'
    }
  },
  components: {
    ShowCase,
    PracticeAreas,
    OurVision,
    ImgA,
    OurAttorneys,
    ContactS,
    
  }
}
</script>