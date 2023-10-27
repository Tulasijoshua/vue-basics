
<template>
  <div class="" :style="{
    width: '100%',
    display: 'flex',
    justifyContent: 'spaceBetween',
    alignItems: 'center',
  }">
    <div>
      <h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>
      <h2 v-for="(name, index) in fullNames" :key="index">{{ name.first }} {{ name.last }}</h2>
      <div v-for="actor in actors" :key="actor.name">
        <h2>{{ actor.name }}</h2>
        <h3 v-for="movie in actor.movies" :key="movie">{{ movie }}</h3>
      </div>
      <!-- <h2 v-for="value in myInfo" :key="value">{{ value }}</h2> -->
      <h2 v-for="(value, key, index) in myInfo" :key="value">{{index}} {{ key }} {{ value }}</h2>
  
      <template v-for="name in names" :key="name">
        <h2>{{name}}</h2>
        <hr />
      </template>
      
      <template v-for="(name, index) in names" :key="index" >
        <h2 v-if="name === 'Bruce'">{{ name }}</h2>
        
      </template>
    </div>
    <practice />
  </div>
</template>

  <script >
  import Practice from './components/Practice.vue';
  export default {
  components: { Practice },
    data() {
      return {
        names: ['Bruce', 'Clark', 'Diana'],
        fullNames: [
          {first: 'Joshua', last: 'Mbawini'},
          {first: 'Tulasi', last: 'Emmanuel'},
          {first: 'Isaac', last: 'Hottor'}
        ],
        actors: [
          {
            name: 'Christian Marfo',
            movies: ['Superman', 'The Prestige']
          },
          {
            name: 'Jedidiah',
            movies: ['Titanic', 'Inception'],
          }
        ],
      }
    },
  }
  </script>
<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}

.flexi {
  width: 100%;
  display: flex;
  justify-content: space-between;
}
</style>
