<template>
  <!-- <pagination></pagination> -->
  <table class="table-auto">
    <caption>All my github repositories</caption>
    <thead>
      <tr>
        <th scope="col">ID</th>
        <th scope="col">Name</th>
        <th scope="col">URL</th>
        <th scope="col">Language</th>
        <th scope="col">Login</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="repo in repos" :key="repo.id">
        <td scope="row">{{ repo.id }}</td>
        <td scope="row">{{ repo.name }}</td>
        <td scope="row">{{ repo.url }}</td>
        <td scope="row">{{ repo.language }}</td>
        <td scope="row">{{ repo.owner.login }}</td>
      </tr>
    </tbody>
  </table>
 
  
</template>

<script>
import axios from 'axios';


export default {
  name:'Repository',
  data() {
    return {
      repos: null,
      currentPage: 1,
      pageSize: 10,
    };
  },
  
  created: function() {
    axios.get('https://api.github.com/users/ArthKate/repos'). then((response) => {
      this.repos = response.data;
    })
  }
};


</script>

<style>
 table {
  table-layout: auto;
  width: 100%;
  border-collapse: inherit;
  border: 1px solid #e5e5e5;
 }
</style>