<template>
    <div class="container">
        <div class="greetings">
            <h1>{{ greeting }}</h1>
        </div>
        <btnSoil text="Start Browsing" shape="round" />
    </div>
</template>


<script>    
import btnSoil from '/src/components/BtnSoil.vue'

export default {
    components: {
        btnSoil
    },
    data () {
        return{
            greeting: "WELCOME"
        }
    }
}
</script>

<style>
    .greetings h1{
        color: white;
        font-size: clamp(6.25rem, 3.125rem + 10vw, 8.75rem);
    }

    .container{
        position: absolute;
        top: 50%;
        transform: translate(0, -50%);
        height: 90%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
</style>
