<template>
    <section id="skills" class="skills-wrapper">
        <pageTitle title="Skills" />
        <div class="skills">
        <ul>
            <li v-for="(skill,index) in skills" :key="index">
            {{ skill.name }}
            </li>
        </ul>
        </div>
    </section>
</template>

<script>
import pageTitle from '@/components/pageTitle'
export default {
    name: 'Skills',
    components: {
        pageTitle
    },
    data() {
        return {
        skills: [
            { name: 'PHP' },
            { name: 'Laravel' },
            { name: 'CakePHP' },
            { name: 'MySQL' },
            { name: 'JavaScript' },
            { name: 'JQuery' },
            { name: 'AWS' },
            { name: 'GitHub' },
            { name: 'Vue.js' },
            { name: 'slack' }
        ]
        }
    }
}
</script>

<style lang='scss' scoped>
@import '@/assets/styles/_mixin.scss';
.skills-wrapper {
    @include section;
}
.skills {
    @include box-wrapper;
}
ul {
    display: grid;
    grid-template-columns: repeat(3, 200px);
    @media (max-width: 670px) {
        grid-template-columns: 200px;
    }
}
li {
    width: 100%;
    text-align: left;
    font-size: 16px;
    padding: 8px 0;
    color: $text-color;
}
</style>