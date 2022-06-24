<template>
  <!-- <div>Hello {{ name }}</div>
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
  <h2 v-if="num === 0">The number is Zero</h2>
  <h2 v-else-if="num < 0">The number is negative</h2>
  <h2 v-else-if="num > 0">The number is positive</h2>
  <h2 v-else>not a number</h2>
   <h2 v-show="showElement">Using v-show</h2>
  <h2 v-for="(name, index) in names" :key="name">{{ index + 1 }} {{ name }}</h2>
  <h2 v-for="name in fullNames" :key="name.first">{{ name.first }} {{ name.last }}</h2>
  <div v-for="actor in actors" :key="actor.name">
    <h2>{{ actor.name }}</h2>
    <h3 v-for="movie in actor.movies" :key="movie">{{ movie }}</h3>
  </div>
  <h2 v-for="(value, key, index) in myInfo" :key="value">{{index +1}} {{key + ':'}} {{ value }} <hr/></h2>  -->
  <h2>{{ name }}</h2>
  <div>
    <button @click="changeName()">Change Name</button>
  </div>
  <h2>{{ count }}</h2>
  <div>
    <button @click="increment(2)">Increment</button>
    <button v-on:click="count -= 1">Decrement</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      // greet: 'Hello',
      name: 'Vishas',
      // channel: `<b>Codevolution</b>`,
      // hack: `<a href="#" onclick="alert('you have been hacked!')">win a prize!</a>`,
      // headingId: 'heading',
      // isDisabled: true,
      // status: 'success',
      // isPromoted: true,
      // isSoldout: true,
      // num: 1,
      // showElement: true,
      // names: ['Bruce', 'Clark', 'Diana'],
      // fullNames: [
      //   { first: 'Bruce', last: 'Wayne' },
      //   { first: 'Clark', last: 'Kent' },
      //   { first: 'Princess', last: 'Diana' },
      // ],
      // actors: [
      //   {
      //     name: 'Christian Bale',
      //     movies: ['Batman', 'The Prestige'],
      //   },
      //   {
      //     name: 'Di Caprio',
      //     movies: ['Titanic', 'Inception'],
      //   },
      // ],
      // myInfo: {
      //   name: 'Osasere',
      //   channel: 'Codevolution',
      //   course: 'Vue3',
      // },
      count: 0,
    };
  },
  methods: {
    changeName() {
      this.name = 'Batman'
    },
    increment(num) {
      this.count += num;
    },
    decrement(num) {
      this.decrement -= num;
    },
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
