<template>
    <div class="dashboard-wrapper">
        <div class="container">dashboard</div>
    </div>
</template>
<script>
export default {
    name: 'Dashboard',
    mounted(){
        this.$api['polkaGetBlocks']()
    }
}
</script>
