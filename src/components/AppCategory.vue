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
            <div class="select">
                <select name="select" id="" v-model="store.seriesOptions">
                    <option @change="$emit('categorySelected')" v-for="(option, index) in seriesOptions" :value="option" :key="index">{{option}}</option>
                               
                </select>
            </div>
</template>

<style lang="scss" scoped>
 
            .select{
                select{
                    
                    border-radius: 1rem;
                    font-size: 2rem;
                    padding: 1rem;
                }
                padding: 1rem;
                margin-bottom: 2rem;
            }

</style>