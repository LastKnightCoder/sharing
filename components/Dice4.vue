<template>
  <div class="container">
    <div class="column">
      <div class="pip"></div>
      <div class="pip"></div>
    </div>
    <div class="column">
      <div class="pip"></div>
      <div class="pip"></div>
    </div>
  </div>
</template>

<style scoped>
.container {
  box-sizing: border;
  width: 200px;
  height: 200px;
  padding: 10px;
  border-radius: 10%;
  box-shadow:
    inset 0 5px white, 
    inset 0 -5px #bbb,
    inset 5px 0 #d7d7d7, 
    inset -5px 0 #d7d7d7;
  background-color: #e7e7e7;
  
  display: flex;
  justify-content: space-between;
}
.column {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.pip {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: #333333;
  box-shadow: inset 0 6px #111, inset 0 -6px #555;
}
</style>