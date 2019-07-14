<template>
    <Panel :class="$style.panel" title="生活服务">
        <section :class="$style.list">
            <div v-for="item in items" :key="item.href" :class="$style.item">
                <img :src="item.src" alt >
                <p :class="$style.text">{{ item.text }}</p>
                <p :class="$style.tip">{{ item.tip }}</p>
            </div>
        </section>
    </Panel>
</template>
<script>
import Panel from '../core/panel.vue'

export default {
    components: {
        Panel
    },
    data() {
        return {
            items: [
                {
                    href: 'home',
                    src:
            '//img12.360buyimg.com/jrpmobile/jfs/t4375/104/1184122472/3976/89741da4/58be8a6eNf10193d0.png?width=135&height=135',
                    text: '惠加油',
                    tip: ''
                },
                {
                    href: 'home',
                    src:
            '//img12.360buyimg.com/jrpmobile/jfs/t4747/185/1901740991/5892/1383fb93/58f57851N17ee6993.jpg?width=132&height=132',
                    text: '小白信用',
                    tip: '全新升级'
                },
                {
                    href: 'home',
                    src:
            '//img12.360buyimg.com/jrpmobile/jfs/t3241/234/8044685271/3713/7b29f77f/58be89c8Nb9d41295.png?width=135&height=135',
                    text: '信用卡还款',
                    tip: ''
                },
                {
                    href: 'home',
                    src:
            '//img12.360buyimg.com/jrpmobile/jfs/t3172/259/7993557249/4351/fd082707/58be8a81Nd7716a06.png?width=135&height=135',
                    text: '卡转让',
                    tip: ''
                },
                {
                    href: 'home',
                    src:
            '//img12.360buyimg.com/jrpmobile/jfs/t3085/320/8107659086/4344/cdbba2dd/58be8acfNdadcaf00.png?width=135&height=135',
                    text: '定期还款',
                    tip: ''
                }
            ]
        }
    }
}
</script>
<style lang="scss" module>
@import "../../css/element.scss";
.panel {
  @include panel;
  .list {
    @include list(row);
    box-sizing: border-box;
    padding-bottom: 40px;
    div {
      width: 20%;
      text-align: center;
      p {
        font-size: 0.65rem;
        color: #666;
        text-overflow: ellipsis;
        white-space: nowrap;
        overflow: hidden;
        margin-top: 0.3rem;
      }
      .tip {
              color: #FF801A;
      }
      img {
        width: 2.25rem;
        height: 2.25rem;
      }
    }
  }
}
</style>

