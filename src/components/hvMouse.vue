<template>
  <i class="mouse icon-mouse"></i>
</template>

<script>
export default {};
</script>

<style lang="scss">
.mouse::before {
  position: absolute;
  left: 0;
  right: 0;
  margin: 0 auto;
  font-size: 40px;
  animation: downUp 0.9s cubic-bezier(0.1, 0.25, 0.1, 1) 0s infinite alternate
    both;
}
@keyframes downUp {
  from {
    transform: translateY(10px);
  }
  to {
    transform: translateY(5px);
  }
}
</style>
