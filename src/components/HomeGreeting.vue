<template>
        <div class="greetings">
            <h1>{{ greeting }}</h1>
        </div>
        <btnSoil text="Start Browsing" />
</template>


<script>    
import btnSoil from './BtnSoil.vue'

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
</style>
