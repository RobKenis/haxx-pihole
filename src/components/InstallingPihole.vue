<template>
  <section data-background-image="assets/keyboard.jpg" data-background-size="cover" data-background-opacity="0.15">
    <div id="content">
      <h3>Installing Pi-hole</h3>
      <pre class="shell"><code data-trim data-noescape>
$ curl -sSL https://install.pi-hole.net | bash
  </code></pre>
    </div>
  </section>
</template>

<script>
export default {
  name: "InstallingPihole",
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Patua+One');

#content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
}

h1 {
  font-family: 'Patua One', serif;
}
</style>