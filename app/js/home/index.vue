<template>
    <div :class="$style.home">
        <heador/>
        <slider/>
        <novice/>
    </div>
</template>

<script>
import Heador from '../public/header.vue'
import Slider from './hslider.vue'
import novice from './novice.vue'

export default {
    components:{
        Heador,
        Slider,
        novice
    }
}
</script>

<style lang="scss" module>
  
</style>
