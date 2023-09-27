<template>
  <div id="content">
    <h2>What is
      <span class="fragment strike" data-fragment-index="1">Pi-hole</span>&nbsp;
      <span class="fragment" data-fragment-index="1">DNS</span>
    </h2>
  </div>
</template>

<script>
export default {
  name: "WhatIsPihole",
};
</script>

<style scoped>
#content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
}
</style>