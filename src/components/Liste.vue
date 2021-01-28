<template>
<div >
   <p>{{ todo }}<img src="../assets/img/remove.svg" alt="icone de suppression" width="20px" /></p>
</div>
</template>

<script>
    export default {
        name: 'Liste',
        props:['todo', 'deleteTask']
    }
</script>

<style>
    img{
        position: absolute;
        top: 20px;
        right: 30px;
    }
</style>