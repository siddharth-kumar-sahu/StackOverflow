<template>
  <div class="loader" />
</template>

<style>
.loader {
  display: inline-block;
  border-radius: 50%;
  height: 30px;
  width: 30px;
  margin: 50px auto;
  border: 3px solid transparent;
  border-top-color: #f48224;
  animation: spin 1s ease infinite;
}

@keyframes spin {
  to {
    -webkit-transform: rotateZ(360deg);
  }
}
</style>
