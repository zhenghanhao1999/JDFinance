<template>
    <section :class="cname">
        <swiper :options="options" :not-next-tick="options.notNextTick">
            <swiper-slide v-for="item in items" :key="item.href">
                <router-link :to="{name:item.href}">
                    <img :src="item.src" alt="">
                </router-link>
            </swiper-slide>
            <div v-if="options.pagination" slot="pagination" class="swiper-pagination"/>
        </swiper>
    </section>
</template>
<script>
// eslint-disable-next-line node/no-extraneous-import
import { swiper, swiperSlide } from 'vue-awesome-swiper'

export default {
    components:{
        swiper,
        swiperSlide
    },
    props:{
        cname:{
            type:String,
            default:''
        },
        options:{
            type:Object,
            default(){
                return{
                    autoplay: true,//自动播放
                    loop:true,//循环
                    pagination: {
                        el:'.swiper-pagination'//指示器
                    },
                    notNextTick:false
                }
            }
        },
        items:{
            type:Array,
            default(){
                return []
            }
        }
    }
}
</script>

<style lang="scss">
@import '~swiper/dist/css/swiper.css';//~让loader能够找到文件

</style>
