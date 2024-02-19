<script>
import CompHeader from './components/header/CompHeader.vue'
import compMain from './components/Main/compMain.vue'
import CompFooter from './components/Footer/CompFooter.vue'


export default {
    components: {
        CompHeader,
        compMain,
        CompFooter

    },
}
</script>

<template>
    <CompHeader />
    <compMain />
    <CompFooter />
</template>

<style>
ul li {
    list-style: none;
}
</style>
