<template>
  <div class="container">
    <search :set-search-name="setSearchName"> </search>

    <userList :search-name="searchName"> </userList>
  </div>
</template>

<script>
  import axios from 'axios'

  import search from './search.vue'
  import userList from './userList.vue'

  export default{
      data(){
         return{
             searchName:''
         }
      },
      methods:{
          setSearchName(searchName){
              this.searchName = searchName
          }
      },
      components:{
        search,
        userList
      }
  }
</script>

<style>
</style>
