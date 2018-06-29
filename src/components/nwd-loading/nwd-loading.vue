<template>
    <div class="nwd-loading" v-show="show">
        <div>{{text}}</div>    
    </div>    
</template>


<script>
    export default {
        props: {
            show: Boolean,
            text: '正在加载中...'
        }
    }
</script>

<style>
.nwd-loading {
    position:absolute;
    margin-left: 40%;
}
</style>
