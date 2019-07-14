<template>
    <div :class="$style.home">
        <heador/>
        <slider/>
        <novice/>
        <borrowing/>
        <finances/>
        <recommend/>
        <service/>
        <footor/>
        <navbar/>
    </div>
</template>

<script>
import Heador from '../public/header.vue'
import footor from '../public/footer.vue'
import navbar from '../public/navbar.vue'
import Slider from './hslider.vue'
import novice from './novice.vue'
import borrowing from './borrowing.vue'
import finances from './finances.vue'
import recommend from './recommend.vue'
import service from './service.vue'

export default {
    components:{
        Heador,
        Slider,
        novice,
        borrowing,
        finances,
        recommend,
        service,
        footor,
        navbar
    }
}
</script>

<style lang="scss" module>
  
</style>
