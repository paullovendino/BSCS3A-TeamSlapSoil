<template>
        <div class="greetings">
            <h1>{{ greeting }}</h1>
        </div>
        <btnSoil text="Start Browsing" />
</template>


<script>
import btnSoil from './btnSoil.vue'

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
        font-size: 140px;
    }
</style>
