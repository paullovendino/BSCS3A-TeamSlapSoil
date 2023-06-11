<template>
    <div class="content-container">
        <div class="borderline">
            <slot></slot>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style>
    .content-container{
        height: 75vh;
        width: 160vh;
        background-color: #ede0d4;
        opacity: .9;
        border-radius: 50px;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .borderline{
        height: 72vh;
        width: 156vh;
        background: transparent;
        border: #CCA481 solid 7px;
        border-radius: 50px;
        display: flex;
        align-items: center;
        justify-content: center;
    }
</style>
