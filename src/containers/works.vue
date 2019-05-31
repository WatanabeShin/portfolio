<template>
    <section id="works" class="works-wrapper">
        <pageTitle title="Works" />
        <div class="works">
        <work-box v-for="work in works" :key="work.link" :item="work" />
        </div>
    </section>
</template>

<script>
import pageTitle from '@/components/pageTitle'
import workBox from '@/components/workBox'
export default {
    name: 'Works',
    components: {
        pageTitle,
        workBox
    },
    data() {
        return {
        works: [
            {
                name: 'はっくまま',
                content:
                    '朝に知ると便利な情報(ゴミ出しや天気占い遅延情報)をLINEに送るbot',
                subContent: 'GAS',
                link: 'https://github.com/WatanabeShin/hack-mama'
            },
            {
                name: 'Portfolio',
                content:
                    'ポートフォリオです。Vue.jsを用いモダンな開発をしてみました。',
                subContent: 'Vue.js',
                link: 'https://github.com/WatanabeShin/portfolio'
            }
        ]
        }
    }
}
</script>

<style lang='scss' scoped>
@import '@/assets/styles/_mixin.scss';
.works-wrapper {
    @include section;
}
.works {
    @include box-wrapper;
}
a {
    text-decoration: none;
}
</style>