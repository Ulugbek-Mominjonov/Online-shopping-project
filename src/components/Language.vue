<template>
  <select >
    <option class="eng" value="1">Eng</option>
    <option value="2">Uzb</option>
  </select>
</template>

<script>
  export default {
    
  }
</script>

<style scoped>
  select {
    border: none;
    padding-left: 3px;
    outline: none;
  }
  select option {
    border: none;
    display: flex;
    align-items: center;
  }
  select option::before {
    display: block;
    content: "";
    width: 18px;
    height: 18px;
    background-size: contain;
  }
  .eng:first-child::before {
    background-image: url("../assets/img/eng.webp");
  }
</style>