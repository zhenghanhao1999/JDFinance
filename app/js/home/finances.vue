<template>
    <Panel :class="$style.panel" title="理财精选">
        <section :class="$style.content">
            <dl v-for="item in items" :class="$style.item" :key="item.title">
                <dt :class="$style.title">{{ item.title }} <span :class="$style.tip">{{ item.sub }}</span></dt>
                <dd :class="$style.red">{{ item.rate }}</dd>
                <dd :class="$style.gray">{{ item.text }}</dd>
            </dl>
        </section>
    </Panel>
</template>
<script>
import Panel from '../core/panel.vue'

export default {
    components:{
        Panel
    },
    data(){
        return {
            items:  [{
                title:'定期理财',
                sub:'理财首选',
                rate:'5.60%',
                text:'历史年化回报率'
            },{
                title:'小白理财',
                sub:'理财首选',
                rate:'4.22%',
                text:'7日年化收益率'
            },
            {
                title:'月月盈',
                sub:'养老保障',
                rate:'5%',
                text:'7日年化收益率'
            },
            {
                title:'小白基金',
                sub:'天天赚钱',
                rate:'4.27%',
                text:'7日年化收益率'
            }
            ]
        }
    },
}
</script>
<style lang="scss" module>
@import '../../css/element.scss';
.panel{
    @include panel;
    .content {
        @include flex(row);
        justify-content: space-around;
        box-sizing: border-box;
        &::after{
            content: " ";
            display: block;
            width: 100%;
            height: 0;
            box-sizing: border-box;
            border-bottom: 0.025rem solid #ddd;
            position: relative;
            top: -4.5rem;
        }
        .item {
            padding: 34px 16px;
            box-sizing: border-box;
            position: relative;
            width: 50%;
           &:after {
               content: ' ';
               width: 1px;
               height: 136px;
               display: block;
               position: absolute;
               top:50%;
               right: 0;
               margin-top: -68px;
               border-right: 1px solid #eee;
           }
           &:nth-child(2n){
               &::after{
                   display: none;
               }
           }
            .title {
                font-size: 30px;
                .tip {
                    font-size: 22px;
                    color: #ff5155;
                    border: 0.025rem solid #ff5155;
                    padding: 0 0.2rem;
                    vertical-align: 0.025rem;
                    margin-left: 0.05rem;
                }
            }
            .red {
                font-weight: 700;
                font-size: 1.1rem;
                height: 1.45rem;
                line-height: 1.45rem;
                color: #FF5155;
                white-space: nowrap;
                text-overflow: ellipsis;
                overflow: hidden;
            }
            .gray {
                color: #999;
                font-size: 24px;
            }
        }
    }
}
</style>
