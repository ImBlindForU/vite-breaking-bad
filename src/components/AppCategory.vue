<script>
    import { store } from "../store";


    export default{
        name: "AppCategory",
        data() {
        return {
            store,
            seriesOptions: ["Breaking Bad", "Better Call Saul"]
        }
    }
}
    
</script>

<template>
        <div class="mini-container">
            <div class="select">
                <select name="select" id="" v-model="store.seriesOptions">
                    <option @change="$emit('categorySelected')" v-for="(option, index) in seriesOptions" :value="option" :key="index">{{option}}</option>
                </select>
                <button class="" @click="$emit('categorySelected')">change</button>
            </div>
        </div>
            
</template>

<style lang="scss" scoped>
        .mini-container{
            display: flex;
            justify-content: center;
            .select{
                select{
                    
                    border-radius: 1rem;
                    font-size: 2rem;
                    padding: 1rem;
                }
                padding: 1rem;
                margin-bottom: 2rem;
            }

            button{
                padding: 1rem;
                font-size: 2rem;
                border-radius: 1rem;
                margin-left:1rem;
            }
        }
            

</style>