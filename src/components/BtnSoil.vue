<template>
    <div>
        <button :class="[type, disabled ? 'disabled' : '']" :disabled="disabled">
            <p>{{ text }}</p>
        </button>
    </div>
</template>

<script>
    export default {
        name: 'btnSoil',
        data(){
            return{

            }
        },
        props: {
            text: String,
            disabled: {
                type: Boolean,
                default: false
            },
            type: {
                type: String,
            }
        }
    }
</script>

<style scoped>
    button{
        background: #B08968;
        color: #E6CCB2;
        padding: 10px;
        border: none;
        box-shadow: 2px 2px rgb(0, 0, 0, 0.5);
    }
    
    button:hover{
        background: #7F5539;
        color: #EDE0D4;
        box-shadow: 3px 3px rgb(0, 0, 0, 0.5);
    }

    .disabled{
        pointer-events: none;
    }

    .disabled:hover{
        pointer-events: none;
    }

    .outlined{
        border: 1px solid black;
        box-shadow: none;
    }

    .outlined:hover{
        border: 1px solid black;
        box-shadow: none;
    }

    .text{
        background: none;
        box-shadow: none;
        color: #7F5539;
    }

    .text:hover{
        box-shadow: none;
        color: #7F5539;
        background: #EDE0D4;
    }

    .tonal{
        box-shadow: none;
        color: #392415;
        background: #E6CCB2;
    }

    .tonal:hover{
        background: #B08968;
        color: #392415;
        box-shadow: none;
    }

    .plain{
        background: none;
        box-shadow: none;
        color: #B08968;
    }

    .plain:hover{
        background: none;
        box-shadow: none;
        color: #392415;
    }
</style>