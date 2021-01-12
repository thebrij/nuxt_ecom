<template>
<div>
    
  <Banner/>
  
  <Category/>
  
  <Footer/>
</div>

  
</template>

<script>
import Banner from '@/components/Banner'
import Footer from '@/components/Footer'
import Category from '@/components/Category'
export default {
  data () {
    return { 
    route: '',
    }
  },
 mounted () {
    window.scrollTo(0, 0);
    this.route = this.$route.name;
  },
}
</script>
