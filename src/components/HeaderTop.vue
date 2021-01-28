<template>
    <div class="header-top">{{ txt }}</div>
</template>

<script>
    export default {
        name: 'HeaderTop',
        data(){
            return {
                txt: "Ma todo liste"
            }
        }
    }
</script>

<style scoped>
    .header-top{
        background: #000;
        color: #F1F1F1;
        height: 70px;
        line-height: 70px;
        text-align: center;
        font-size: 2rem;
    }
</style>