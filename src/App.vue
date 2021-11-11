<template>
  <div id="app">
    <MoviesList :list="moviesList" />
  </div>
</template>

<script>
import { mapActions, mapGetters } from "vuex";
import MoviesList from "@/components/MoviesList";

export default {
  name: "App",
  components: {
    MoviesList,
  },
  computed: {
    ...mapGetters("movies", ["moviesList"]),
  },
  methods: {
    ...mapActions("movies", ["fetchMovies"]),
  },
};
</script>

<style>
#app {
  font-family: Arial, Helvetica, sans-serif;
  -webkit-font-smothing: antialiased;
  -moz-osx-font-smothing: grayscale;
}
</style>
