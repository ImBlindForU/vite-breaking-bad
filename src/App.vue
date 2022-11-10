<script >
  import AppHeader from "./components/AppHeader.vue";
  import AppMain from "./components/AppMain.vue";
  import axios from "axios";
  import { store } from "./store";

  export  default{
    components:{
      AppHeader,
      AppMain,
    },
    data(){
      return{
        store
      }
    },
    created() {
      axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
        this.store.characters = resp.data
      console.log(this.store.characters);
      
    });
    }
  }
</script>

<template>
  <AppHeader />
  <AppMain />

</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
