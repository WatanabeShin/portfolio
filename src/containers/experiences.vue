<template>
    <section id="experiences" class="experiences-wrapper">
        <pageTitle title="Experiences" />
        <div class="box-wrapper">
        <table>
            <tbody>
            <tr v-for="(experience, index) in experiences" :key="index">
                <th>{{ experience.term }}</th>
                <td>{{ experience.key }}</td>
                <td class="last-td">
                    {{ experience.value }}
                </td>
            </tr>
            </tbody>
        </table>
        </div>
    </section>
</template>

<script>
import pageTitle from '@/components/pageTitle'
export default {
    name: 'Experiences',
    components: {
        pageTitle
    },
    data() {
        return {
        experiences: [
            {
            key: 'EBA inc.',
            value: '正社員',
            term: '2017/09 ~ Present'
            },
            {
            key: '某通信会社',
            value: '客先常駐　オペレーション用サイトの新規開発',
            term: '2017/10 ~ 2018/09'
            },
            {
            key: '某ベンチャー企業',
            value: '客先常駐　キュレーションサイトの新規開発',
            term: '2018/10 ~ 2019/03'
            }
        ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/_color.scss';
@import '@/assets/styles/_mixin.scss';
.experiences-wrapper {
    @include section;
}
.box-wrapper {
    @include box-wrapper;
    color: $text-color;
    table {
        display: inline-block;
        text-align: left;
    }
    th {
        padding-right: 20px;
        font-weight: normal;
        color: $sub-text-color;
    }
    td {
        font-size: 20px;
        padding: 5px 8px 5px 0px;
    }
    }
    a {
    text-decoration: none;
}
/*スマートフォン*/
@media (max-width: 820px) {
    .box-wrapper {
        th {
        display: block;
        padding: 0px 16px;
        }
        td {
        display: block;
        font-size: 16px;
        width: 100%;
        padding: 5px 16px;
        }
        .last-td {
        border-bottom: 1px solid $border-color;
        }
    }
}
</style>