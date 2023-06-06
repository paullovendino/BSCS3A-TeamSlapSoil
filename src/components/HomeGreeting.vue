<template>
        <div class="greetings">
            <h1>{{ greeting }}</h1>
        </div>
</template>

<script>
export default {
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