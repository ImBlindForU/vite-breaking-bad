<script>
    import CardCharacter from "./CardCharacter.vue";
    import { store } from "../store";


    export default{
        name: "CardList",
        components :{
            CardCharacter,
        },
        data(){
            return{
                store
             }
        },
    }
</script>



<template>

    <div class="row-cards" >
        <h3>Found 62 characters</h3>
        <CardCharacter v-for="character in store.characters" :key="character.char_id" :character="character"/>
    </div>

</template>

<style lang="scss" scoped>
    .container-fluid{
        .container{
            .row-cards{

                h3{
                    width: 110%;
                    background-color: #212529;
                    color: white;
                    padding: 2rem;
                    font-size: 2rem;
                    margin-bottom: 2rem;


                }
                display: flex;
                flex-wrap: wrap;
                background-color: white;
                padding: 4rem;
                padding-top: 6rem;
            }
        }
    }
</style>