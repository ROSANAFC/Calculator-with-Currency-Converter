<template>
    <button type="button" class="btn" >
      {{ symbols }}
    </button>
  </template>
  
  <script>
    export default {
      name: 'ButtonInput',
      props: {
        symbols: String
      }
    }
  </script>
  
  <style scoped lang="postcss">
    .btn {
        background: rgb(98, 153, 160);
        height: 2em;
        width: 2em;
        border-radius: 1% rgb(56, 55, 55);
    }
  </style>