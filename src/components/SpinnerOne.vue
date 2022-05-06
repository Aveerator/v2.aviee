<template>
  <div class="body">
    <div class="spinner"><slot></slot></div>
  </div>
</template>

<style>
.body {
}

.spinner {
  text-align: center;
  animation-name: spin, depth;
  animation-timing-function: linear;
  animation-iteration-count: infinite;
  animation-duration: 3s;
  text-decoration: none;
  font-weight: bold;
}

@keyframes spin {
  from {
    transform: rotateY(0deg);
  }

  to {
    transform: rotateY(-360deg);
  }
}
</style>
