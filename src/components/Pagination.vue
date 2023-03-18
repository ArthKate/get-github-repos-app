<template>
  <div>
    <div class="pagination-row">
      <span v-for="(item, index) in new Array" :key="index">
        <button class="pagination-btn">{{ index + 1 }}</button>
      </span>
      
    </div>
  </div>

</template>


<script>
export default {
  name: 'pagination',
}

</script>


<style>
.pagination-btn {
  padding: 8px;
  margin: 2px;
  border-radius: 3px;
  font-size: 1em;
  cursor: pointer;
}
</style>