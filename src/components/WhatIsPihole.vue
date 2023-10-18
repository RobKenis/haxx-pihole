<template>
  <section>
    <section data-background-image="assets/raspi.jpg" data-background-size="cover" data-background-opacity="0.15">
      <div id="content">
        <h2>What is a Pi-hole</h2>
        <ul id="what-is-pi-hole">
          <li class="fragment">Raspberry <span class="highlight">Pi</span></li>
          <li class="fragment">DNS Sink<span class="highlight">hole</span></li>
        </ul>
      </div>
    </section>
    <section data-background-image="assets/signpost.jpg" data-background-size="cover" data-background-opacity="0.15">
      <div id="content">
        <h2>What is DNS</h2>
        <ul>
          <li class="fragment">axxes.com <span class="fragment">&#8594; 142.93.236.160</span></li>
          <li class="fragment highlight">googleadservices.com <span class="fragment">&#8594; 0.0.0.0</span></li>
        </ul>
      </div>
    </section>
  </section>
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

#what-is-pi-hole {
  list-style: circle;
  font-size: 5rem;
}

.highlight {
  color: #e74c3c;
  font-weight: bold;
}
</style>