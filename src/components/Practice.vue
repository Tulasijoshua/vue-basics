<template>
    <div>
        <h2 v-for="(name, index) in names" :key="index">{{ index }} {{ name }}</h2>
        <h3 v-for="(name, index) in fullNames" :key="index"> {{ name.last }}</h3>
        <div v-for="(actor, index) in actors" :key="index">
           <h2>{{ actor.name }}</h2>
            <h3 v-for="(movie, index) in actor.movies" :key="index">{{ movie }}</h3>
        </div>

        <template v-for="(name, index) in names" :key="index">
            <h2 >{{ name }}</h2>
            <hr />
        </template>

        <template v-for="(name, index) in names" :key="index">
            <h3 v-if="name === 'Emmanuel'">{{ name }}</h3>
        </template>
        
    </div>
</template>

<script>
    export default {
        name: 'Practice',
        data() {
            return {
                names: ['Joshua', 'Emmanuel', 'Jedidiah'],
                fullNames: [
                    {first: 'Joshua', last: 'Mbawini'},
                    {first: 'Emmanuel', last: 'Tulasi'},
                    {first: 'Isaac', last: 'Hottor'},
                ],
                actors: [
                    {
                        name: 'Joshua',
                        movies: ['Superman', 'Batman']
                    },
                    {
                        name: 'Tulasi',
                        movies: ['Terminator', 'The Jenitor']
                    }
                ]
            }
        }
    }
</script>

<style scoped>

</style>