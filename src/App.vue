<template>
  <div class="project-title">
    <h1>{{ title }}</h1>
    <p>{{ desc }}</p>
  </div>
  <Repository />
  <Pagination />


  
</template>

<script>
import Repository from './components/Repository.vue';
import Pagination from './components/Pagination.vue';


export default {
  name: 'App',
  components: {
    Repository, Pagination
  },
  data() {
    return {
      title: 'Github Repositories',
      desc: 'Using Vue Js, RestAPi and Axios',


    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}

.project-title {
  background: #57cc99;
  height: 150px;
  color: #fff;
  text-align: center;
  padding: 40px;
}

h1 {
  font-weight:bolder;
}

p {
  margin-top: 10px;
}

</style>
