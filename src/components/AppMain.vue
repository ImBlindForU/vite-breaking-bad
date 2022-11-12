<script>
    import CardList from "./CardList.vue";
    import AppCategory from "./AppCategory.vue";
    import axios from "axios";
    import { store } from "../store";
    
    export default{
        name: "AppMain",
        data(){
            return{
                store
            }
        },
        components :{
            CardList,
            AppCategory,
            
        },created() {
        this.getCharacters();
        },
        methods:{
            getCharacters(){
                let apiUrl = "https://www.breakingbadapi.com/api/characters?"
 
                if(this.store.seriesOptions != ""){
                    if(this.store.seriesOptions === "Breaking Bad"){
                        apiUrl += `category=Breaking Bad`;
                    }else if(this.store.seriesOptions === "Better Call Saul"){
                        apiUrl += `category=Better Call Saul`;

                    }    
            

                } 


                axios.get(apiUrl).then((resp) => {
                this.store.characters = resp.data
                console.log(apiUrl);
                });
            }
        }
    }
</script>

<template>
    <div class="container-fluid">
        <div class="container">
            <AppCategory @categorySelected="getCharacters"/>
            <CardList />
            
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .container-fluid{
        .container{
            margin-top: 10rem;
            .row-cards{
                display: flex;
            }
        }
    }
</style>