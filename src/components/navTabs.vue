<template>
    <div class="tab-content" v-show="title == selectedTitle">
        <slot></slot>
    </div>
</template>

<script>
    import { inject } from 'vue'

    export default {
        name: 'Tabs',
        props: {
            'title': String,
        },
        setup(){
            const selectedTitle = inject('selectedTitle')

            return{
                selectedTitle,
            }
        }
    }
</script>

<style scoped>
    .tab-content{
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        margin-top: 40px;
    }
</style>
