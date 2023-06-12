<template>
  <div :class="[shape, hovereffect, 'hover', disabled? 'disabled' : '']">
    <slot></slot>
  </div>
</template>

<script>
export default {
    name: 'Hover',
    props: {
      hovereffect: String,
      disabled: false,
      shape: String,
  },
}
</script>

<style scoped>
    .hover {
      background-color: #b08968;
      color: white;
      border:solid 3px #7F5539;
      cursor: pointer;
      padding: 10px;
      transition:ease-in-out .2s;
      min-width: 40px;
    }

    .round{
      border-radius: 10px;
    }

    .hover:hover {
      background-color: #EDE0D4;
      color: #7F5539;
    }
    .underlined:hover{
      text-decoration: underline;
      color: white ;
    }
    .text-color:hover{
      color: black;
    }
    .zoom-in:hover{
      transform: scale(1.5);
    }
    .zoom-out:hover{
      transform: scale(0.5);
    }
    .shadow:hover{
      box-shadow: 3px 3px rgb(0, 0, 0, 0.5);
    }
    .right-tilt:hover{
      transform: rotate(40deg);
    }
    .left-tilt:hover{
      transform: rotate(-40deg);
    }
    .border:hover{
      border: solid 5px #7F5539;
      border-radius: 0px;
    }

    .disabled:hover{
      transform: none;
      box-shadow: none;
      background: #b08968;
      color: white;
      cursor: default;
    }
</style>
