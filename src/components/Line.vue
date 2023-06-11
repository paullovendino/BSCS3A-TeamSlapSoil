<template>
    <div :class="alignment">
    </div>
</template>

<script>
    export default{
        name:"Line",
        props: {
            alignment: String,
        }
    }
</script>

<style scoped>
    div{
        width: 100%;
        height: 1px;
        background-color: #7F5539;
    }

    .horizontal{
        background-color: #7F5539;
        height: 100%;
        width: 1px;
    }
</style>
