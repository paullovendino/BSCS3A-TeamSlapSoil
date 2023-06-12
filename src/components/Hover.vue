<template>
  <div :class="['Hover', type]" :disabled="disabled">
    <h2>Hover Me!</h2>
  </div>
</template>

<script>
export default {
    name: 'Hover',
    props: {
      type: String,
      disabled: false
  },
}
</script>

<style scoped>
    .Hover {
      background-color: #b08968;
      color: white;
      border:solid 3px #7F5539;
      border-radius: 10px;
      cursor: pointer;
      font-size: 20px;
      padding: 15px;
      transition:ease-in-out .2s;
    }
    .ChangeBackgroundColor:hover {
      background-color: #EDE0D4;
      color: #7F5539;
    }
    .Underlined:hover{
      text-decoration: underline;
      color: white ;
    }
    .ChangeTextColor:hover{
      color: black;
    }
    .ZoomIn:hover{
      transform: scale(1.5);
    }
    .ZoomOut:hover{
      transform: scale(0.5);
    }
    .TextZoom h2:hover{
      transform: scale(1.2);
      transition: .3s;
    }
    .RightTilt:hover{
      transform: rotate(40deg);
    }
    .LeftTilt:hover{
      transform: rotate(-40deg);
    }
    .BorderLine:hover{
      border: solid 10px #7F5539;
      border-radius: 0px;
    }
</style>
