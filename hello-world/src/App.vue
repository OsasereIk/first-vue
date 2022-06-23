<template>
  <div>Hello {{ name }}</div>
  <div v-html="channel"></div>
  <div v-html="hack"></div>
  <h2 v-bind:id="headingId">Header</h2>
  <button v-bind:disabled="isDisabled">bind</button>
  <h2 class="underline">underline text</h2>
  <h2 class="underline" :class="status">status</h2>
  <h2 :class="isPromoted && 'promoted'">Promoted Movie</h2>
  <h2 :class="isSoldout ? 'sold-out' : 'new'">Soldout Movie</h2>
  <h2 :class="['new', 'promoted']">Newly Promoted Movie</h2>
  <h2 :class="[isPromoted && 'promoted', isSoldout ? 'sold-out' : 'new ']">Array conditional movie</h2>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      greet: 'Hello',
      name: 'Vishas',
      channel: `<b>Codevolution</b>`,
      hack: `<a href="#" onclick="alert('you have been hacked!')">win a prize!</a>`,
      headingId: 'heading',
      isDisabled: true,
      status: 'success',
      isPromoted: true,
      isSoldout: true,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.new {
  color: green;
}

.sold-out {
  color: crimson;
}
</style>
