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

        <CardCharacter v-for="character in store.characters" :key="character.char_id" :character="character"/>
    </div>

</template>

<style lang="scss" scoped>
    .container-fluid{
        .container{
            .row-cards{
                display: flex;
                flex-wrap: wrap;
            }
        }
    }
</style>